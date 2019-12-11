# 文字识别SDK简介<a name="ocr_04_0016"></a>

## 文字识别概述<a name="section1582503120018"></a>

文字识别（Optical Character Recognition，简称OCR）将图片或扫描件中的文字识别成可编辑的文本。可代替人工录入，提升业务效率。支持身份证、驾驶证、行驶证、发票、英文海关单据、通用表格、通用文字等场景文字识别。

文字识别以开放API（Application Programming Interface，应用程序编程接口）的方式提供给用户，用户通过实时访问和调用API获取推理结果，帮助用户提升业务效率。

## SDK概述<a name="section191232404117"></a>

文字识别软件开发工具包（Optical Character Recognition Software Development Kit，简称OCR SDK）是对文字识别提供的REST API进行的封装，以简化用户的开发工作。用户直接调用OCR SDK提供的接口函数即可实现使用文字识别服务业务能力的目的。

## 接口与API对应关系<a name="section121947299416"></a>

文字识别接口与API对应关系请参见[表1](#table47650414583)。

**表 1**  接口与API对应关系表

<a name="table47650414583"></a>
<table><thead align="left"><tr id="row77666475813"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p95715105588"><a name="p95715105588"></a><a name="p95715105588"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p1757210175816"><a name="p1757210175816"></a><a name="p1757210175816"></a>API</p>
</th>
</tr>
</thead>
<tbody><tr id="row19951628942"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1938017301948"><a name="p1938017301948"></a><a name="p1938017301948"></a>通用表格识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1638013301841"><a name="p1638013301841"></a><a name="p1638013301841"></a>POST /v1.0/ocr/general-table</p>
</td>
</tr>
<tr id="row5869477410"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p2095005610416"><a name="p2095005610416"></a><a name="p2095005610416"></a>通用文字识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5950165616418"><a name="p5950165616418"></a><a name="p5950165616418"></a>POST /v1.0/ocr/general-text</p>
</td>
</tr>
<tr id="row141521841154"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p20581191614517"><a name="p20581191614517"></a><a name="p20581191614517"></a>网络图片识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p11581216052"><a name="p11581216052"></a><a name="p11581216052"></a>POST /v1.0/ocr/web-image</p>
</td>
</tr>
<tr id="row211110227517"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p111119221556"><a name="p111119221556"></a><a name="p111119221556"></a>智能分类识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1211192217512"><a name="p1211192217512"></a><a name="p1211192217512"></a>POST /v1.0/ocr/auto-classification</p>
</td>
</tr>
<tr id="row76131749367"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p339115591469"><a name="p339115591469"></a><a name="p339115591469"></a>手写文字识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p139185914610"><a name="p139185914610"></a><a name="p139185914610"></a>POST /v1.0/ocr/handwriting</p>
</td>
</tr>
<tr id="row1176617412585"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p19735727176"><a name="p19735727176"></a><a name="p19735727176"></a>身份证识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p373515279719"><a name="p373515279719"></a><a name="p373515279719"></a>POST /v1.0/ocr/id-card</p>
</td>
</tr>
<tr id="row476616475811"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1618953418710"><a name="p1618953418710"></a><a name="p1618953418710"></a>行驶证识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p101891034679"><a name="p101891034679"></a><a name="p101891034679"></a>POST /v1.0/ocr/vehicle-license</p>
</td>
</tr>
<tr id="row197666417586"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p441418402714"><a name="p441418402714"></a><a name="p441418402714"></a>驾驶证识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p164141240171"><a name="p164141240171"></a><a name="p164141240171"></a>POST /v1.0/ocr/driver-license</p>
</td>
</tr>
<tr id="row127671943580"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p142111254176"><a name="p142111254176"></a><a name="p142111254176"></a>护照识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p6211954875"><a name="p6211954875"></a><a name="p6211954875"></a>POST /v1.0/ocr/passport</p>
</td>
</tr>
<tr id="row12767642587"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p7284131212813"><a name="p7284131212813"></a><a name="p7284131212813"></a>银行卡识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p12284212482"><a name="p12284212482"></a><a name="p12284212482"></a>POST /v1.0/ocr/bankcard</p>
</td>
</tr>
<tr id="row198105216428"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p20191182164212"><a name="p20191182164212"></a><a name="p20191182164212"></a>营业执照识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p19191122114215"><a name="p19191122114215"></a><a name="p19191122114215"></a>POST /v1.0/ocr/business-license</p>
</td>
</tr>
<tr id="row1568552511422"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p246213774219"><a name="p246213774219"></a><a name="p246213774219"></a>道路运输证识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p946283718420"><a name="p946283718420"></a><a name="p946283718420"></a>POST /v1.0/ocr/transportation-license</p>
</td>
</tr>
<tr id="row17308165117424"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p863717316438"><a name="p863717316438"></a><a name="p863717316438"></a>车牌识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p163720315439"><a name="p163720315439"></a><a name="p163720315439"></a>POST /v1.0/ocr/plate-number</p>
</td>
</tr>
<tr id="row185451150174616"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p753221217716"><a name="p753221217716"></a><a name="p753221217716"></a>增值税发票识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p853219121378"><a name="p853219121378"></a><a name="p853219121378"></a>POST /v1.0/ocr/vat-invoice</p>
</td>
</tr>
<tr id="row81231238191711"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1512423851712"><a name="p1512423851712"></a><a name="p1512423851712"></a>机动车销售发票识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5124183814172"><a name="p5124183814172"></a><a name="p5124183814172"></a>POST /v1.0/ocr/mvs-invoice</p>
</td>
</tr>
<tr id="row1317919404177"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p10522726164716"><a name="p10522726164716"></a><a name="p10522726164716"></a>出租车发票识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5522172616479"><a name="p5522172616479"></a><a name="p5522172616479"></a>POST /v1.0/ocr/taxi-invoice</p>
</td>
</tr>
<tr id="row510013536910"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1380703874714"><a name="p1380703874714"></a><a name="p1380703874714"></a>火车票识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p880723816474"><a name="p880723816474"></a><a name="p880723816474"></a>POST /v1.0/ocr/train-ticket</p>
</td>
</tr>
<tr id="row16154199122519"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p493489162712"><a name="p493489162712"></a><a name="p493489162712"></a>定额发票识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1386818540259"><a name="p1386818540259"></a><a name="p1386818540259"></a>POST /v1.0/ocr/quota-invoice</p>
</td>
</tr>
<tr id="row3490145842516"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p6935264278"><a name="p6935264278"></a><a name="p6935264278"></a>车辆通行费发票识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p2015513910254"><a name="p2015513910254"></a><a name="p2015513910254"></a>POST /v1.0/ocr/toll-invoice</p>
</td>
</tr>
<tr id="row19868135417253"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p0368118102718"><a name="p0368118102718"></a><a name="p0368118102718"></a>飞机行程单识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p12490358192513"><a name="p12490358192513"></a><a name="p12490358192513"></a>POST  /v1.0/ocr/flight-itinerary</p>
</td>
</tr>
<tr id="row16367526252"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1353216124716"><a name="p1353216124716"></a><a name="p1353216124716"></a>英文海关单据识别</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p253210121176"><a name="p253210121176"></a><a name="p253210121176"></a>POST /v1.0/ocr/action/ocr_form</p>
</td>
</tr>
</tbody>
</table>

