# PHP语言API示例<a name="ocr_03_0136"></a>

本示例以通用表格识别为例介绍如何使用PHP调用API，如需调用其他API，请替换代码中的“https://\{endpoint\}/v2/\{project\_id\}/ocr/general-table”字段。

```
<?php

function TokenRequest() {
    $url = "https://{endpoint}/v2/{project_id}/ocr/general-table";
    $token = "用户获取得到的实际token值";
    $imagePath = __DIR__.'/data/general-table.jpg';
    
    
    $options = [];

    $data = array();
    if (stripos($imagePath, 'http://') !== false || stripos($imagePath, 'https://') !== false) {
        $data['url'] = $imagePath;
    } else {
        if($fp = fopen($imagePath,"rb", 0))
        {
            $gambar = fread($fp,filesize($imagePath));
            fclose($fp);

            $fileBase64 = chunk_split(base64_encode($gambar));
        } else {
            echo "图片读取错误";
            return;
        }
        $data['image'] = $fileBase64;
    }

    if(!empty($options)){
        $data = array_merge($data, $options);
    }

    $curl = curl_init();
    $headers = array(
        "Content-Type:application/json",
        "X-Auth-Token:" . $token
    );

    /* 设置请求体 */
    curl_setopt($curl, CURLOPT_URL, $url);
    curl_setopt($curl, CURLOPT_HTTPHEADER, $headers);
    curl_setopt($curl, CURLOPT_POST, 1);
    curl_setopt($curl, CURLOPT_POSTFIELDS, json_encode($data));
    curl_setopt($curl, CURLOPT_RETURNTRANSFER, TRUE);
    curl_setopt($curl, CURLOPT_NOBODY, FALSE);
    curl_setopt($curl, CURLOPT_SSL_VERIFYPEER, false);
    curl_setopt($curl, CURLOPT_TIMEOUT, 30);

    $response = curl_exec($curl);
    $status = curl_getinfo($curl, CURLINFO_HTTP_CODE);
    curl_close($curl);
    echo $response;
}

TokenRequest();
```

**表 1**  参数说明

<a name="table143571850893"></a>
<table><thead align="left"><tr id="row1335814502094"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="p17358135012911"><a name="p17358135012911"></a><a name="p17358135012911"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="p20358850595"><a name="p20358850595"></a><a name="p20358850595"></a>参数说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row935835019916"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p1635835017911"><a name="p1635835017911"></a><a name="p1635835017911"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p3358165016919"><a name="p3358165016919"></a><a name="p3358165016919"></a>API请求URL，例如本示例中https://{endpoint}/v2/{project_id}/ocr/general-table。</p>
</td>
</tr>
<tr id="row16673135214128"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p26731452101211"><a name="p26731452101211"></a><a name="p26731452101211"></a>token</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p4840556171113"><a name="p4840556171113"></a><a name="p4840556171113"></a>Token是用户的访问令牌，承载了用户的身份、权限等信息，用户调用API接口时，需要使用Token进行鉴权。</p>
<p id="p1133721105312"><a name="p1133721105312"></a><a name="p1133721105312"></a>获取Token方法请参见<a href="https://support.huaweicloud.com/qs-ocr/ocr_05_0003.html" target="_blank" rel="noopener noreferrer">快速入门</a>。</p>
</td>
</tr>
<tr id="row1422447141315"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p22241273138"><a name="p22241273138"></a><a name="p22241273138"></a>imagePath</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p9224576135"><a name="p9224576135"></a><a name="p9224576135"></a>图片路径。支持图片文件路径或图片url路径。其中，图片的url路径支持公网http/https url或OBS提供的url。</p>
</td>
</tr>
</tbody>
</table>

