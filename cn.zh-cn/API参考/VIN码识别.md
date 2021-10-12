# VIN码识别<a name="ocr_03_0121"></a>

## 功能介绍<a name="section214354317318"></a>

识别图片中的车架号信息，并将识别结果以json格式返回给用户。该接口的使用限制请参见[约束与限制](https://support.huaweicloud.com/productdesc-ocr/ocr_01_0006.html#section14)，详细使用指导请参见[OCR服务使用简介](https://support.huaweicloud.com/qs-ocr/ocr_05_0001.html)章节。

**图 1**  VIN码识别示例图<a name="fig54613362514"></a>  
![](figures/VIN码识别示例图.png "VIN码识别示例图")

## 调试<a name="section15544724131819"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=OCR&api=RecognizeVIN)中调试该接口。

## 前提条件<a name="section17299143617379"></a>

在使用VIN码识别之前，需要您完成服务申请和认证鉴权，具体操作流程请参见[申请服务](申请服务.md)和[认证鉴权](认证鉴权.md)章节。

>![](public_sys-resources/icon-note.gif) **说明：** 
>用户首次使用需要先[申请开通](https://console.huaweicloud.com/ocr/?region=cn-north-4#/ocr/overview)。服务只需要开通一次即可，后面使用时无需再次申请。如未开通服务，调用服务时会提示ModelArts.4204报错，请在调用服务前先进入控制台开通服务，并注意开通服务区域与调用服务的区域保持一致。

## URI<a name="section1788318311840"></a>

POST https://\{endpoint\}/v2/\{project\_id\}/ocr/vin

**表 1**  路径参数

<a name="table1757114411019"></a>
<table><thead align="left"><tr id="row244311551906"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p15443125512018"><a name="p15443125512018"></a><a name="p15443125512018"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p14431555504"><a name="p14431555504"></a><a name="p14431555504"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1444145517013"><a name="p1444145517013"></a><a name="p1444145517013"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row613718443010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p191375441708"><a name="p191375441708"></a><a name="p191375441708"></a>endpoint</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p81375441015"><a name="p81375441015"></a><a name="p81375441015"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1928291782612"><a name="p1928291782612"></a><a name="p1928291782612"></a>指定承载REST服务端点的服务器域名或IP，不同服务不同区域的endpoint不同，您可以从<a href="终端节点.md">终端节点</a>中获取。</p>
<p id="p85151503246"><a name="p85151503246"></a><a name="p85151503246"></a>例如，OCR服务在<span class="parmvalue" id="parmvalue832520377716"><a name="parmvalue832520377716"></a><a name="parmvalue832520377716"></a>“华北-北京四”</span>区域的<span class="parmname" id="parmname211216411978"><a name="parmname211216411978"></a><a name="parmname211216411978"></a>“endpoint”</span>为<span class="parmvalue" id="parmvalue998414713715"><a name="parmvalue998414713715"></a><a name="parmvalue998414713715"></a>“ocr.cn-north-4.myhuaweicloud.com”</span>。</p>
</td>
</tr>
<tr id="row935272033518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p335222016354"><a name="p335222016354"></a><a name="p335222016354"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p735211208354"><a name="p735211208354"></a><a name="p735211208354"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p9352620133512"><a name="p9352620133512"></a><a name="p9352620133512"></a>项目ID，您可以从<a href="获取项目ID.md">获取项目ID</a>中获取。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="section20373546918"></a>

**表 2**  请求Header参数

<a name="table723982483111"></a>
<table><thead align="left"><tr id="row52401924193111"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p1924082410316"><a name="p1924082410316"></a><a name="p1924082410316"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="p12404242315"><a name="p12404242315"></a><a name="p12404242315"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1924019242314"><a name="p1924019242314"></a><a name="p1924019242314"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.4"><p id="p92404245319"><a name="p92404245319"></a><a name="p92404245319"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1624062423110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p82401524193115"><a name="p82401524193115"></a><a name="p82401524193115"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p1224017242315"><a name="p1224017242315"></a><a name="p1224017242315"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1424016242318"><a name="p1424016242318"></a><a name="p1424016242318"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p62408249311"><a name="p62408249311"></a><a name="p62408249311"></a>用户Token。</p>
<p id="p87711532113213"><a name="p87711532113213"></a><a name="p87711532113213"></a>Token认证就是在调用API的时候将Token加到请求消息头，从而通过身份认证，获得操作API的权限，响应消息头中X-Subject-Token的值即为Token。</p>
</td>
</tr>
<tr id="row853215489116"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p620162911477"><a name="p620162911477"></a><a name="p620162911477"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p122082984710"><a name="p122082984710"></a><a name="p122082984710"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p12017295472"><a name="p12017295472"></a><a name="p12017295472"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p62022944710"><a name="p62022944710"></a><a name="p62022944710"></a>发送的实体的MIME类型，参数值为“application/json”。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="table13634105116210"></a>
<table><thead align="left"><tr id="row58136515213"><th class="cellrowborder" valign="top" width="15.770000000000001%" id="mcps1.2.5.1.1"><p id="p1081316514215"><a name="p1081316514215"></a><a name="p1081316514215"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.09%" id="mcps1.2.5.1.2"><p id="p681313519219"><a name="p681313519219"></a><a name="p681313519219"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="13.270000000000001%" id="mcps1.2.5.1.3"><p id="p1781318512023"><a name="p1781318512023"></a><a name="p1781318512023"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="54.87%" id="mcps1.2.5.1.4"><p id="p281445112216"><a name="p281445112216"></a><a name="p281445112216"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2814951126"><td class="cellrowborder" valign="top" width="15.770000000000001%" headers="mcps1.2.5.1.1 "><p id="p781413512214"><a name="p781413512214"></a><a name="p781413512214"></a>image</p>
</td>
<td class="cellrowborder" valign="top" width="16.09%" headers="mcps1.2.5.1.2 "><p id="p5814551626"><a name="p5814551626"></a><a name="p5814551626"></a>否，该参数与url二选一</p>
</td>
<td class="cellrowborder" valign="top" width="13.270000000000001%" headers="mcps1.2.5.1.3 "><p id="p1881455120218"><a name="p1881455120218"></a><a name="p1881455120218"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.87%" headers="mcps1.2.5.1.4 "><p id="p17315937101918"><a name="p17315937101918"></a><a name="p17315937101918"></a>图像数据，base64编码，要求base64编码后大小不超过10MB。图片最小边不小于15px，最长边不超过4096px，支持JPEG、JPG、PNG、BMP、TIFF格式。</p>
</td>
</tr>
<tr id="row16799203015443"><td class="cellrowborder" valign="top" width="15.770000000000001%" headers="mcps1.2.5.1.1 "><p id="p15453133284416"><a name="p15453133284416"></a><a name="p15453133284416"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="16.09%" headers="mcps1.2.5.1.2 "><p id="p64531532164415"><a name="p64531532164415"></a><a name="p64531532164415"></a>否，该参数与image二选一</p>
</td>
<td class="cellrowborder" valign="top" width="13.270000000000001%" headers="mcps1.2.5.1.3 "><p id="p845383213448"><a name="p845383213448"></a><a name="p845383213448"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.87%" headers="mcps1.2.5.1.4 "><p id="p86827584714"><a name="p86827584714"></a><a name="p86827584714"></a>图片的url路径，目前支持：</p>
<a name="ul42174521583"></a><a name="ul42174521583"></a><ul id="ul42174521583"><li>公网http/https url</li><li>OBS提供的url，使用OBS数据需要进行授权。包括对服务授权、临时授权、匿名公开授权，详情参见<a href="配置OBS访问权限.md">配置OBS访问权限</a>。</li></ul>
<div class="note" id="note1822116578284"><a name="note1822116578284"></a><a name="note1822116578284"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul99367258155"></a><a name="ul99367258155"></a><ul id="ul99367258155"><li>接口响应时间依赖于图片的下载时间，如果图片下载时间过长，会返回接口调用失败。</li></ul>
<a name="ul156081829151514"></a><a name="ul156081829151514"></a><ul id="ul156081829151514"><li>请保证被检测图片所在的存储服务稳定可靠，推荐使用OBS服务存储图片数据。</li></ul>
</div></div>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section1870005811125"></a>

根据识别的结果，可能有不同的HTTP响应状态码（status code），状态码和响应参数说明如下。

**状态码： 200**

**表 4**  响应Body参数

<a name="responseParameter"></a>
<table><thead align="left"><tr id="row1989536554"><th class="cellrowborder" valign="top" width="24.05%" id="mcps1.2.4.1.1"><p id="p139899313552"><a name="p139899313552"></a><a name="p139899313552"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.57%" id="mcps1.2.4.1.2"><p id="p1199043185516"><a name="p1199043185516"></a><a name="p1199043185516"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="59.38%" id="mcps1.2.4.1.3"><p id="p159909317558"><a name="p159909317558"></a><a name="p159909317558"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row498913195512"><td class="cellrowborder" valign="top" width="24.05%" headers="mcps1.2.4.1.1 "><p id="p299093105510"><a name="p299093105510"></a><a name="p299093105510"></a>result</p>
</td>
<td class="cellrowborder" valign="top" width="16.57%" headers="mcps1.2.4.1.2 "><p id="p169902315518"><a name="p169902315518"></a><a name="p169902315518"></a><a href="#response_VINResponseBodyItem">VINResult</a> object</p>
</td>
<td class="cellrowborder" valign="top" width="59.38%" headers="mcps1.2.4.1.3 "><p id="p39918313556"><a name="p39918313556"></a><a name="p39918313556"></a>调用成功时表示调用结果。</p>
<p id="p1199153165517"><a name="p1199153165517"></a><a name="p1199153165517"></a>调用失败时无此字段。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  VINResult

<a name="response_VINResponseBodyItem"></a>
<table><thead align="left"><tr id="row5991103135516"><th class="cellrowborder" valign="top" width="24.05%" id="mcps1.2.4.1.1"><p id="p999143185512"><a name="p999143185512"></a><a name="p999143185512"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.57%" id="mcps1.2.4.1.2"><p id="p99927315558"><a name="p99927315558"></a><a name="p99927315558"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="59.38%" id="mcps1.2.4.1.3"><p id="p5992230551"><a name="p5992230551"></a><a name="p5992230551"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row399116345516"><td class="cellrowborder" valign="top" width="24.05%" headers="mcps1.2.4.1.1 "><p id="p19921036559"><a name="p19921036559"></a><a name="p19921036559"></a>vin</p>
</td>
<td class="cellrowborder" valign="top" width="16.57%" headers="mcps1.2.4.1.2 "><p id="p109921315519"><a name="p109921315519"></a><a name="p109921315519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.38%" headers="mcps1.2.4.1.3 "><p id="p499263145518"><a name="p499263145518"></a><a name="p499263145518"></a>识别检测到的车架号。</p>
</td>
</tr>
</tbody>
</table>

**状态码： 400**

**表 6**  响应Body参数

<a name="table14116152816914"></a>
<table><thead align="left"><tr id="row104241536131018"><th class="cellrowborder" valign="top" width="24.05%" id="mcps1.2.4.1.1"><p id="p1161161304115"><a name="p1161161304115"></a><a name="p1161161304115"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.57%" id="mcps1.2.4.1.2"><p id="p5161913174119"><a name="p5161913174119"></a><a name="p5161913174119"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="59.38%" id="mcps1.2.4.1.3"><p id="p11618137419"><a name="p11618137419"></a><a name="p11618137419"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row13331423104618"><td class="cellrowborder" valign="top" width="24.05%" headers="mcps1.2.4.1.1 "><p id="p812923044615"><a name="p812923044615"></a><a name="p812923044615"></a>error_code</p>
</td>
<td class="cellrowborder" valign="top" width="16.57%" headers="mcps1.2.4.1.2 "><p id="p612953017464"><a name="p612953017464"></a><a name="p612953017464"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.38%" headers="mcps1.2.4.1.3 "><p id="p1812983084610"><a name="p1812983084610"></a><a name="p1812983084610"></a>调用失败时的错误码，具体请参见<a href="错误码.md">错误码</a>。</p>
<p id="p143717550113"><a name="p143717550113"></a><a name="p143717550113"></a>当出现错误码<span class="parmname" id="parmname179861912181220"><a name="parmname179861912181220"></a><a name="parmname179861912181220"></a>“ModelArts.4204”</span>时，请参考<a href="https://support.huaweicloud.com/ocr_faq/ocr_01_0031.html" target="_blank" rel="noopener noreferrer">为什么调用API时提示“ModelArts.4204”？</a>章节。</p>
<p id="p111299307468"><a name="p111299307468"></a><a name="p111299307468"></a>调用成功时无此字段。</p>
</td>
</tr>
<tr id="row256927124618"><td class="cellrowborder" valign="top" width="24.05%" headers="mcps1.2.4.1.1 "><p id="p3129103014465"><a name="p3129103014465"></a><a name="p3129103014465"></a>error_msg</p>
</td>
<td class="cellrowborder" valign="top" width="16.57%" headers="mcps1.2.4.1.2 "><p id="p412915302464"><a name="p412915302464"></a><a name="p412915302464"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.38%" headers="mcps1.2.4.1.3 "><p id="p16129630204616"><a name="p16129630204616"></a><a name="p16129630204616"></a>调用失败时的错误信息。</p>
<p id="p1812943019467"><a name="p1812943019467"></a><a name="p1812943019467"></a>调用成功时无此字段。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section1080017111613"></a>

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   “endpoint“即调用API的请求地址，不同服务不同区域的“endpoint“不同，具体请参见[终端节点](终端节点.md)。
>    例如，VIN码识别服务部署在“华北-北京四“区域的“endpoint“为“ocr.cn-north-4.myhuaweicloud.com“，请求URL为“https://ocr.cn-north-4.myhuaweicloud.com/v2/\{project\_id\}/ocr/vin“，“project\_id“为项目ID，获取方法请参见[获取项目ID](获取项目ID.md)
>-   如何获取Token具体操作请参见[构造请求](构造请求.md)。

-   请求样例（方式一：使用图片的base64编码）

    ```
    POST https://{endpoint}/v2/{project_id}/ocr/vin
     
    Request Header:   
    Content-Type: application/json
    X-Auth-Token: MIINRwYJKoZIhvcNAQcCoIINODCCDTQCAQExDTALBglghkgBZQMEAgEwgguVBgkqhkiG...
    Request Body:
    {
        "image":"/9j/4AAQSkZJRgABAgEASABIAAD/4RFZRXhpZgAATU0AKgAAAA..."
    }
    ```

-   请求样例（方式二：使用图片URL）

    ```
    POST https://{endpoint}/v2/{project_id}/ocr/vin
     
    Request Header:   
    Content-Type: application/json
    X-Auth-Token: MIINRwYJKoZIhvcNAQcCoIINODCCDTQCAQExDTALBglghkgBZQMEAgEwgguVBgkqhkiG...
    Request Body:
    {
        "url":"https://BucketName.obs.xxxx.com/ObjectName"
    }
    ```

-   Python3语言请求代码示例（其他语言参照下列示例编写或使用OCR SDK）

    ```
    # encoding:utf-8
    
    import requests
    import base64
    
    url = "https://{endpoint}/v2/{project_id}/ocr/vin"
    token = "用户获取得到的实际token值"
    headers = {'Content-Type': 'application/json', 'X-Auth-Token': token}
    
    imagepath = r'./data/vin-demo.png'
    with open(imagepath, "rb") as bin_data:
        image_data = bin_data.read()
    image_base64 = base64.b64encode(image_data).decode("utf-8")  # 使用图片的base64编码
    payload = {"image": image_base64}  # url与image参数二选一
    response = requests.post(url, headers=headers, json=payload)
    print(response.text)
    ```


## 响应示例<a name="section7587788419"></a>

**状态码：200**

成功响应示例

```
{
    "result": {
        "vin": "JN8BYXXXXXXXX7207"
    }
}
```

**状态码：400**

失败响应示例

```
{
    "error_code": "AIS.0103", 
    "error_msg": "The image size does not meet the requirements."
}
```

## 状态码<a name="section1559819539185"></a>

<a name="table59811812815"></a>
<table><thead align="left"><tr id="row109811881280"><th class="cellrowborder" valign="top" width="30%" id="mcps1.1.3.1.1"><p id="p6981987818"><a name="p6981987818"></a><a name="p6981987818"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.1.3.1.2"><p id="p39821086818"><a name="p39821086818"></a><a name="p39821086818"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row99821816814"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.1.3.1.1 "><p id="p39821881387"><a name="p39821881387"></a><a name="p39821881387"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.1.3.1.2 "><p id="p20982189818"><a name="p20982189818"></a><a name="p20982189818"></a>成功响应。</p>
</td>
</tr>
<tr id="row477317212816"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.1.3.1.1 "><p id="p577317219819"><a name="p577317219819"></a><a name="p577317219819"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.1.3.1.2 "><p id="p177311219818"><a name="p177311219818"></a><a name="p177311219818"></a>失败响应。</p>
</td>
</tr>
</tbody>
</table>

状态码请参见[状态码](状态码.md)。

## 错误码<a name="section545533743312"></a>

错误码请参见[错误码](错误码.md)。

