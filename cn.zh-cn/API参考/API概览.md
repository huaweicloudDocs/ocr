# API概览<a name="ocr_03_0047"></a>

通过使用文字识别服务的自研API，您可以使用文字识别服务的所有功能，如[表1](#table4171135310353)所示。

文字识别服务当前支持通用类、证件类、票据类和智能分类四种不同类型的接口。您可以通过[在线体验](https://lab.huaweicloud.com/solutiondetail_567)，体验接口的识别效果。

对于固定板式的图片，如果当前接口不满足您的业务需求，可以使用ModelArts Pro服务提供的[文字识别套件](https://support.huaweicloud.com/usermanual-modelartspro/modelartspro_01_0007.html)，零代码搭建出专属的API，详细操作请参见[视频指导](https://support.huaweicloud.com/modelartspro_video/index.html)。

**表 1**  接口说明

<a name="table4171135310353"></a>
<table><thead align="left"><tr id="row986713053614"><th class="cellrowborder" valign="top" width="9.45%" id="mcps1.2.5.1.1"><p id="p2402014431"><a name="p2402014431"></a><a name="p2402014431"></a>类别</p>
</th>
<th class="cellrowborder" valign="top" width="16.82%" id="mcps1.2.5.1.2"><p id="p21906145190"><a name="p21906145190"></a><a name="p21906145190"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="50.36000000000001%" id="mcps1.2.5.1.3"><p id="p12867193018363"><a name="p12867193018363"></a><a name="p12867193018363"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="23.369999999999997%" id="mcps1.2.5.1.4"><p id="p727419563519"><a name="p727419563519"></a><a name="p727419563519"></a>部署区域</p>
</th>
</tr>
</thead>
<tbody><tr id="row077602318497"><td class="cellrowborder" rowspan="5" valign="top" width="9.45%" headers="mcps1.2.5.1.1 "><p id="p155205311339"><a name="p155205311339"></a><a name="p155205311339"></a>通用类</p>
</td>
<td class="cellrowborder" valign="top" width="16.82%" headers="mcps1.2.5.1.2 "><p id="p12948202512493"><a name="p12948202512493"></a><a name="p12948202512493"></a><a href="通用表格识别.md">通用表格识别</a></p>
</td>
<td class="cellrowborder" valign="top" width="50.36000000000001%" headers="mcps1.2.5.1.3 "><p id="p1094842520493"><a name="p1094842520493"></a><a name="p1094842520493"></a>识别表格图片上的文字内容，并返回识别的结构化结果。</p>
</td>
<td class="cellrowborder" valign="top" width="23.369999999999997%" headers="mcps1.2.5.1.4 "><p id="p152745567511"><a name="p152745567511"></a><a name="p152745567511"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row126121330124917"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p87274020514"><a name="p87274020514"></a><a name="p87274020514"></a><a href="通用文字识别.md">通用文字识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p117271905511"><a name="p117271905511"></a><a name="p117271905511"></a>识别图片上的文字内容，并返回识别的文字和坐标。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p15274756152"><a name="p15274756152"></a><a name="p15274756152"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row564131591416"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p167951449184717"><a name="p167951449184717"></a><a name="p167951449184717"></a><a href="网络图片识别.md">网络图片识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p4194174715266"><a name="p4194174715266"></a><a name="p4194174715266"></a>识别网络图片中的文字内容，并以json格式返回识别的结构化结果。该接口的使用限制请参见<a href="https://support.huaweicloud.com/productdesc-ocr/ocr_01_0006.html#section2" target="_blank" rel="noopener noreferrer">约束与限制</a>，详细使用指导请参见<a href="https://support.huaweicloud.com/qs-ocr/ocr_05_0001.html" target="_blank" rel="noopener noreferrer">OCR服务使用简介</a>章节。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p18758131231111"><a name="p18758131231111"></a><a name="p18758131231111"></a>华北-北京四(cn-north-4)</p>
<p id="p122742561352"><a name="p122742561352"></a><a name="p122742561352"></a>华南-广州(cn-south-1)</p>
<p id="p118041454710"><a name="p118041454710"></a><a name="p118041454710"></a>华东-上海一(cn-east-3)</p>
</td>
</tr>
<tr id="row4348145316142"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p195114491645"><a name="p195114491645"></a><a name="p195114491645"></a><a href="智能分类识别.md">智能分类识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p24399514525"><a name="p24399514525"></a><a name="p24399514525"></a>检测定位图片上指定要识别的票证（票据、证件或其他文字载体），并以json格式返回识别的结构化结果。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p8274556658"><a name="p8274556658"></a><a name="p8274556658"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row11265163517218"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p5785335164910"><a name="p5785335164910"></a><a name="p5785335164910"></a><a href="手写文字识别.md">手写文字识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p14785173594916"><a name="p14785173594916"></a><a name="p14785173594916"></a>识别手写文字图片中的文字内容。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p13274135615515"><a name="p13274135615515"></a><a name="p13274135615515"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row13197183161311"><td class="cellrowborder" rowspan="10" valign="top" width="9.45%" headers="mcps1.2.5.1.1 "><p id="p820317560314"><a name="p820317560314"></a><a name="p820317560314"></a>证件类</p>
</td>
<td class="cellrowborder" valign="top" width="16.82%" headers="mcps1.2.5.1.2 "><p id="p14921101319137"><a name="p14921101319137"></a><a name="p14921101319137"></a><a href="身份证识别.md">身份证识别</a></p>
</td>
<td class="cellrowborder" valign="top" width="50.36000000000001%" headers="mcps1.2.5.1.3 "><p id="p11921161321311"><a name="p11921161321311"></a><a name="p11921161321311"></a>识别身份证图片中正面与反面的文字内容，并返回识别的文字和坐标。</p>
</td>
<td class="cellrowborder" valign="top" width="23.369999999999997%" headers="mcps1.2.5.1.4 "><p id="p162743561356"><a name="p162743561356"></a><a name="p162743561356"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row7479555131512"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1092141331311"><a name="p1092141331311"></a><a name="p1092141331311"></a><a href="行驶证识别.md">行驶证识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p169211613121313"><a name="p169211613121313"></a><a name="p169211613121313"></a>识别行驶证图片中主页与副页的文字内容，并返回识别的文字和坐标。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p727415561855"><a name="p727415561855"></a><a name="p727415561855"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row4223131019137"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p18921913131318"><a name="p18921913131318"></a><a name="p18921913131318"></a><a href="驾驶证识别.md">驾驶证识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p892191311313"><a name="p892191311313"></a><a name="p892191311313"></a>识别驾驶证图片中主页与副页的文字内容，并返回识别的文字和坐标。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p627415568519"><a name="p627415568519"></a><a name="p627415568519"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row025172417176"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p3788783317"><a name="p3788783317"></a><a name="p3788783317"></a><a href="护照识别.md">护照识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p12354613252"><a name="p12354613252"></a><a name="p12354613252"></a>识别护照首页图片中的文字信息，并以json格式返回识别的结构化结果。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p927413561759"><a name="p927413561759"></a><a name="p927413561759"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row75621538101719"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p122131292715"><a name="p122131292715"></a><a name="p122131292715"></a><a href="银行卡识别.md">银行卡识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p121677503254"><a name="p121677503254"></a><a name="p121677503254"></a>识别银行卡上的关键文字信息，并以json格式返回识别的结构化结果。该接口的使用限制请参见<a href="https://support.huaweicloud.com/productdesc-ocr/ocr_01_0006.html#section9" target="_blank" rel="noopener noreferrer">约束与限制</a>，详细使用指导请参见<a href="https://support.huaweicloud.com/qs-ocr/ocr_05_0001.html" target="_blank" rel="noopener noreferrer">OCR服务使用简介</a>章节。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p1127415564514"><a name="p1127415564514"></a><a name="p1127415564514"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row6533131516186"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1493501216278"><a name="p1493501216278"></a><a name="p1493501216278"></a><a href="营业执照识别.md">营业执照识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p841184862520"><a name="p841184862520"></a><a name="p841184862520"></a>识别营业执照首页图片中的文字信息，并以json格式返回识别的结构化结果。该接口的使用限制请参见<a href="https://support.huaweicloud.com/productdesc-ocr/ocr_01_0006.html#section10" target="_blank" rel="noopener noreferrer">约束与限制</a>，详细使用指导请参见<a href="https://support.huaweicloud.com/qs-ocr/ocr_05_0001.html" target="_blank" rel="noopener noreferrer">OCR服务使用简介</a>章节。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p18274105613510"><a name="p18274105613510"></a><a name="p18274105613510"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row139223193198"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p041691402718"><a name="p041691402718"></a><a name="p041691402718"></a><a href="道路运输证识别.md">道路运输证识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p9409134319257"><a name="p9409134319257"></a><a name="p9409134319257"></a>识别道路运输证首页中的文字信息，并以json格式返回识别的结构化结果。该接口的使用限制请参见<a href="https://support.huaweicloud.com/productdesc-ocr/ocr_01_0006.html#section12" target="_blank" rel="noopener noreferrer">约束与限制</a>，详细使用指导请参见<a href="https://support.huaweicloud.com/qs-ocr/ocr_05_0001.html" target="_blank" rel="noopener noreferrer">OCR服务使用简介</a>章节。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p12274856750"><a name="p12274856750"></a><a name="p12274856750"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row1173070155118"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p127241001519"><a name="p127241001519"></a><a name="p127241001519"></a><a href="车牌识别.md">车牌识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p772416015111"><a name="p772416015111"></a><a name="p772416015111"></a>识别车牌图片中的车牌信息，并返回其坐标和内容。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p32742561657"><a name="p32742561657"></a><a name="p32742561657"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row43563593199"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p123561259161915"><a name="p123561259161915"></a><a name="p123561259161915"></a><a href="名片识别.md">名片识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p235615911917"><a name="p235615911917"></a><a name="p235615911917"></a>识别名片图片上的文字信息，并返回识别的结构化结果。支持对多种不同版式名片进行结构化信息提取。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p22749561510"><a name="p22749561510"></a><a name="p22749561510"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row759418411204"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p65940411204"><a name="p65940411204"></a><a name="p65940411204"></a><a href="VIN码识别.md">VIN码识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p16594114162015"><a name="p16594114162015"></a><a name="p16594114162015"></a>识别图片中的车架号信息，并将识别结果返回给用户。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p5274556859"><a name="p5274556859"></a><a name="p5274556859"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row3617125714239"><td class="cellrowborder" rowspan="9" valign="top" width="9.45%" headers="mcps1.2.5.1.1 "><p id="p129300293520"><a name="p129300293520"></a><a name="p129300293520"></a>票据类</p>
</td>
<td class="cellrowborder" valign="top" width="16.82%" headers="mcps1.2.5.1.2 "><p id="p187797231496"><a name="p187797231496"></a><a name="p187797231496"></a><a href="增值税发票识别.md">增值税发票识别</a></p>
</td>
<td class="cellrowborder" valign="top" width="50.36000000000001%" headers="mcps1.2.5.1.3 "><p id="p9779162320492"><a name="p9779162320492"></a><a name="p9779162320492"></a>识别增值税发票图片中的文字内容，并返回识别的结构化结果。</p>
</td>
<td class="cellrowborder" valign="top" width="23.369999999999997%" headers="mcps1.2.5.1.4 "><p id="p12274256755"><a name="p12274256755"></a><a name="p12274256755"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row126353019393"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p116401507395"><a name="p116401507395"></a><a name="p116401507395"></a><a href="发票验真.md">发票验真</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p17640140163911"><a name="p17640140163911"></a><a name="p17640140163911"></a>支持9种增值税发票的信息核验。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p1264000133910"><a name="p1264000133910"></a><a name="p1264000133910"></a>华北-北京四(cn-north-4)</p>
<p id="p7265122010409"><a name="p7265122010409"></a><a name="p7265122010409"></a>华东-上海一(cn-east-3)</p>
</td>
</tr>
<tr id="row860433513191"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p187251906510"><a name="p187251906510"></a><a name="p187251906510"></a><a href="机动车销售发票识别.md">机动车销售发票识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p9727170195115"><a name="p9727170195115"></a><a name="p9727170195115"></a>识别机动车销售发票图片中的文字内容，并返回识别的结构化结果。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p16274156450"><a name="p16274156450"></a><a name="p16274156450"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row127619252019"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p581241711279"><a name="p581241711279"></a><a name="p581241711279"></a><a href="出租车发票识别.md">出租车发票识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p17439545172618"><a name="p17439545172618"></a><a name="p17439545172618"></a>识别出租车发票中的文字信息，并以json格式返回识别的结构化结果。该接口的使用限制请参见<a href="https://support.huaweicloud.com/productdesc-ocr/ocr_01_0006.html#section17" target="_blank" rel="noopener noreferrer">约束与限制</a>，详细使用指导请参见<a href="https://support.huaweicloud.com/qs-ocr/ocr_05_0001.html" target="_blank" rel="noopener noreferrer">OCR服务使用简介</a>章节。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p12274195610511"><a name="p12274195610511"></a><a name="p12274195610511"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row1511643810207"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p10612172813462"><a name="p10612172813462"></a><a name="p10612172813462"></a><a href="火车票识别.md">火车票识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p166371052142519"><a name="p166371052142519"></a><a name="p166371052142519"></a>识别火车票中的文字信息，并以json格式返回识别的结构化结果。该接口的使用限制请参见<a href="https://support.huaweicloud.com/productdesc-ocr/ocr_01_0006.html#section17" target="_blank" rel="noopener noreferrer">约束与限制</a>，详细使用指导请参见<a href="https://support.huaweicloud.com/qs-ocr/ocr_05_0001.html" target="_blank" rel="noopener noreferrer">OCR服务使用简介</a>章节。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p5274956359"><a name="p5274956359"></a><a name="p5274956359"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row915115586228"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p493489162712"><a name="p493489162712"></a><a name="p493489162712"></a><a href="定额发票识别.md">定额发票识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p1386818540259"><a name="p1386818540259"></a><a name="p1386818540259"></a>识别定额发票中的文字信息，并以json格式返回识别的结构化结果。该接口的使用限制请参见<a href="https://support.huaweicloud.com/productdesc-ocr/ocr_01_0006.html#section17" target="_blank" rel="noopener noreferrer">约束与限制</a>，详细使用指导请参见<a href="https://support.huaweicloud.com/qs-ocr/ocr_05_0001.html" target="_blank" rel="noopener noreferrer">OCR服务使用简介</a>章节。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p3274356759"><a name="p3274356759"></a><a name="p3274356759"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row814651116215"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p6935264278"><a name="p6935264278"></a><a name="p6935264278"></a><a href="车辆通行费发票识别.md">车辆通行费发票识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p1835119915019"><a name="p1835119915019"></a><a name="p1835119915019"></a>识别车辆通行费发票中的关键文字信息，并以json格式返回识别的结构化结果。该接口的使用限制请参见<a href="https://support.huaweicloud.com/productdesc-ocr/ocr_01_0006.html#section17" target="_blank" rel="noopener noreferrer">约束与限制</a>，详细使用指导请参见<a href="https://support.huaweicloud.com/qs-ocr/ocr_05_0001.html" target="_blank" rel="noopener noreferrer">OCR服务使用简介</a>章节。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p327465616515"><a name="p327465616515"></a><a name="p327465616515"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
<tr id="row1915502532116"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p0368118102718"><a name="p0368118102718"></a><a name="p0368118102718"></a><a href="飞机行程单识别.md">飞机行程单识别</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p12490358192513"><a name="p12490358192513"></a><a name="p12490358192513"></a>识别飞机行程单中的文字信息，并以json格式返回识别的结构化结果。该接口的使用限制请参见<a href="https://support.huaweicloud.com/productdesc-ocr/ocr_01_0006.html#section17" target="_blank" rel="noopener noreferrer">约束与限制</a>，详细使用指导请参见<a href="https://support.huaweicloud.com/qs-ocr/ocr_05_0001.html" target="_blank" rel="noopener noreferrer">OCR服务使用简介</a>章节。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p122743569511"><a name="p122743569511"></a><a name="p122743569511"></a>华北-北京四(cn-north-4)</p>
</td>
</tr>
</tbody>
</table>

