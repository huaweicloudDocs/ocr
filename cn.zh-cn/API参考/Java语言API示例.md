# Java语言API示例<a name="ocr_03_0129"></a>

本示例以通用表格识别为例介绍如何使用Java调用API，如需调用其他API，请替换代码中的“https://\{endpoint\}/v2/\{project\_id\}/ocr/general-table”字段。

```
package OCRDemo;
import com.huawei.ais.sdk.util.HttpClientUtils;

import java.io.File;
import java.io.IOException;
import java.net.URISyntaxException;

import org.apache.http.Header;
import org.apache.http.HttpResponse;
import org.apache.http.entity.StringEntity;
import org.apache.commons.codec.binary.Base64;
import org.apache.commons.io.FileUtils;
import org.apache.commons.io.IOUtils;
import com.alibaba.fastjson.JSONObject;

import org.apache.http.entity.ContentType;
import org.apache.http.message.BasicHeader;

/**
 * 此demo仅供测试使用，强烈建议使用SDK
 * 使用前需配置依赖jar包。jar包可通过下载SDK获取
 */

public class OCRDemo {
	public static void main(String[] args) throws URISyntaxException, UnsupportedOperationException, IOException{
		TokenDemo();
	}
	
	public static void TokenDemo() throws URISyntaxException, UnsupportedOperationException, IOException {

		String url = "https://{endpoint}/v2/{project_id}/ocr/general-table";
		String token = "用户获取得到的实际token值";
		String imgPath = "./data/general-table-demo.png"; //File path or URL of the image to be recognized.
		
        JSONObject params = new JSONObject();
		try {
			if (imgPath.indexOf("http://") != -1 || imgPath.indexOf("https://") != -1) {
				params.put("url", imgPath);
			} else {
				byte[] fileData = FileUtils.readFileToByteArray(new File(imgPath));
				String fileBase64Str = Base64.encodeBase64String(fileData);
				params.put("image", fileBase64Str);
			}

			Header[] headers = new Header[]{new BasicHeader("X-Auth-Token", token), new BasicHeader("Content-Type", ContentType.APPLICATION_JSON.toString())};
			StringEntity stringEntity = new StringEntity(params.toJSONString(), "utf-8");
			HttpResponse response = HttpClientUtils.post(url, headers, stringEntity);
			String content = IOUtils.toString(response.getEntity().getContent(), "utf-8");
			System.out.println(content); 
		}
		catch (Exception e) {
			e.printStackTrace();
		}
	}
}

```

**表 1**  参数说明

<a name="table6112164517716"></a>
<table><thead align="left"><tr id="row1112104511714"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="p101127457713"><a name="p101127457713"></a><a name="p101127457713"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="p1911212459718"><a name="p1911212459718"></a><a name="p1911212459718"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row13991026293"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p125127282098"><a name="p125127282098"></a><a name="p125127282098"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p151211281192"><a name="p151211281192"></a><a name="p151211281192"></a>API请求URL，例如本示例中https://{endpoint}/v2/{project_id}/ocr/general-table。</p>
</td>
</tr>
<tr id="row41121145279"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p311284513713"><a name="p311284513713"></a><a name="p311284513713"></a>token</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p4840556171113"><a name="p4840556171113"></a><a name="p4840556171113"></a>Token是用户的访问令牌，承载了用户的身份、权限等信息，用户调用API接口时，需要使用Token进行鉴权。</p>
<p id="p1133721105312"><a name="p1133721105312"></a><a name="p1133721105312"></a>获取Token方法请参见<a href="https://support.huaweicloud.com/qs-ocr/ocr_05_0003.html" target="_blank" rel="noopener noreferrer">快速入门</a>。</p>
</td>
</tr>
<tr id="row15041916911"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p14501119794"><a name="p14501119794"></a><a name="p14501119794"></a>imagePath</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p135021914917"><a name="p135021914917"></a><a name="p135021914917"></a>图片路径。支持图片文件路径或图片url路径。其中，图片的url路径支持公网http/https url或OBS提供的url。</p>
</td>
</tr>
</tbody>
</table>

