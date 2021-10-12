# Python3语言API示例<a name="ocr_03_0127"></a>

本示例以通用表格识别为例介绍如何使用Python3调用API，如需调用其他API，请替换代码中的“https://\{endpoint\}/v2/\{project\_id\}/ocr/general-table”字段。

```
# encoding:utf-8

import requests
import base64

url = "https://{endpoint}/v2/{project_id}/ocr/general-table"
token = "用户获取得到的实际token值"
headers = {'Content-Type': 'application/json', 'X-Auth-Token': token}

imagepath = r'./data/general-table-demo.png'
with open(imagepath, "rb") as bin_data:
    image_data = bin_data.read()
image_base64 = base64.b64encode(image_data).decode("utf-8")  # 使用图片的base64编码
payload = {"image": image_base64}  # url与image参数二选一

response = requests.post(url, headers=headers, json=payload)
print(response.text)
```

**表 1**  参数说明

<a name="table81324219537"></a>
<table><thead align="left"><tr id="row111331921195312"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="p11331921205312"><a name="p11331921205312"></a><a name="p11331921205312"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="p3133152117537"><a name="p3133152117537"></a><a name="p3133152117537"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row161334219536"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p2133122125317"><a name="p2133122125317"></a><a name="p2133122125317"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p101331521115315"><a name="p101331521115315"></a><a name="p101331521115315"></a>API请求URL，例如本示例中https://{endpoint}/v2/{project_id}/ocr/general-table。</p>
</td>
</tr>
<tr id="row713352119530"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p141333211539"><a name="p141333211539"></a><a name="p141333211539"></a>token</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p4840556171113"><a name="p4840556171113"></a><a name="p4840556171113"></a>Token是用户的访问令牌，承载了用户的身份、权限等信息，用户调用API接口时，需要使用Token进行鉴权。</p>
<p id="p1133721105312"><a name="p1133721105312"></a><a name="p1133721105312"></a>获取Token方法请参见<a href="https://support.huaweicloud.com/qs-ocr/ocr_05_0003.html" target="_blank" rel="noopener noreferrer">快速入门</a>。</p>
</td>
</tr>
<tr id="row4677351237"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p767813512310"><a name="p767813512310"></a><a name="p767813512310"></a>imagepath</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p1967895113313"><a name="p1967895113313"></a><a name="p1967895113313"></a>图片路径。支持图片文件路径或图片url路径。其中，图片的url路径支持公网http/https url或OBS提供的url。</p>
</td>
</tr>
</tbody>
</table>

