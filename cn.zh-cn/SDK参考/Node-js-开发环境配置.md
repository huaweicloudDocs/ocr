# Node.js 开发环境配置<a name="ocr_04_0033"></a>

## 操作场景<a name="section1560105320810"></a>

文字识别服务Node.js SDK支持Windows、Linux、Mac等操作系统。本节以Windows系统为例进行环境配置，要求的操作环境请参见[表1](#table129385511897)。

**表 1**  准备环境

<a name="table129385511897"></a>
<table><thead align="left"><tr id="row129391511996"><th class="cellrowborder" valign="top" width="40.02%" id="mcps1.2.3.1.1"><p id="p95932451011"><a name="p95932451011"></a><a name="p95932451011"></a>准备环境</p>
</th>
<th class="cellrowborder" valign="top" width="59.98%" id="mcps1.2.3.1.2"><p id="p1858114312102"><a name="p1858114312102"></a><a name="p1858114312102"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row275091831015"><td class="cellrowborder" valign="top" width="40.02%" headers="mcps1.2.3.1.1 "><p id="p256912101317"><a name="p256912101317"></a><a name="p256912101317"></a>操作系统</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.3.1.2 "><p id="p35709231310"><a name="p35709231310"></a><a name="p35709231310"></a>Windows系统，推荐Windows 7及以上版本。</p>
</td>
</tr>
<tr id="row1093995110917"><td class="cellrowborder" valign="top" width="40.02%" headers="mcps1.2.3.1.1 "><p id="p057017221319"><a name="p057017221319"></a><a name="p057017221319"></a>安装Node.js</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.3.1.2 "><p id="p157217261311"><a name="p157217261311"></a><a name="p157217261311"></a>Node.js版本建议使用Node.js v10.13.0及以上版本。</p>
</td>
</tr>
<tr id="row109392051892"><td class="cellrowborder" valign="top" width="40.02%" headers="mcps1.2.3.1.1 "><p id="p135728211132"><a name="p135728211132"></a><a name="p135728211132"></a>安装Node.js依赖库</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.3.1.2 "><p id="p0573152141313"><a name="p0573152141313"></a><a name="p0573152141313"></a>OCR Node.js SDK依赖第三方库request、moment、moment-timezone包。</p>
</td>
</tr>
</tbody>
</table>

## 操作步骤<a name="section636542121215"></a>

以下步骤以win7环境安装Node.js v10.13.0为例，已安装Node.js或者更高版本并且安装了依赖包请跳过本章节。

1.  配置Node.js。

    Node.js下载地址：[http://nodejs.cn/download/](http://nodejs.cn/download/)，下载Node.js最新版本。

    配置Node.js环境变量: 右键“计算机\>属性\>高级系统设置\>环境变量”在Path中添加C:\\Program Files\\nodejs（node.exe默认安装路径）。

2.  验证Node.js。

    在系统命令行输入node –v查看Node.js的版本，如果出现了当前的版本号，即为配置成功。

3.  配置cnpm与配置国内软件库。

    ```
    $ npm install -g cnpm --registry=https://registry.npm.taobao.org
    ```

    如果已经配置，请直接跳转到[4](#li960805518424)。

4.  <a name="li960805518424"></a>安装依赖包。

    在Node.js项目的根目录中，shift+鼠标右键，选择“在此处打开命令窗口”，执行下列命令。

    ```
    cnpm install request –save
    cnpm install moment --save
    cnpm install moment-timezone --save
    ```


