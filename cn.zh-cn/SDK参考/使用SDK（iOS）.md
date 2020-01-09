# 使用SDK（iOS）<a name="ocr_04_0027"></a>

用户使用服务的认证方式有Token和AK/SK两种，获取认证消息请参考[认证鉴权](https://support.huaweicloud.com/api-ocr/ocr_03_0005.html)。本章节主要包含Token和AK/SK两种方式使用SDK进行示例说明。

在OCR SDK开发工具包地址：[https://developer.huaweicloud.com/sdk?OCR](https://developer.huaweicloud.com/sdk?OCR)，选择OCR iOS SDK工具包下载并解压。

>![](public_sys-resources/icon-note.gif) **说明：**   
>用户首次使用需要先[申请开通](https://console.huaweicloud.com/ocr/?region=cn-north-4&locale=zh-cn#/ocr/management/main)该服务。（服务只需要开通一次即可，后面使用时无需再次申请。）  

## AK/SK认证方式<a name="section20574102575613"></a>

本节以身份证识别服务为例介绍如何以AK/SK认证方式使用SDK。

1.  获取AK/SK，具体步骤请参见[认证鉴权\>AK/SK认证](https://support.huaweicloud.com/api-ocr/ocr_03_0005.html#section1)。
2.  配置iOS SDK的AK/SK。

    根据获取的AK/SK，修改Demo工程“ViewController.m”文件中akskOcrService函数的“AK”和“SK”的值，请参见[图1](#fig4540185611343)。

    **图 1**  修改ViewController.m文件参数<a name="fig4540185611343"></a>  
    ![](figures/修改ViewController-m文件参数.png "修改ViewController-m文件参数")

3.  如使用本地图片文件进行识别，修改ViewController.m文件中akskOcrService函数中image参数，请参见[图1](#fig4540185611343)。如使用SDK默认图片则不需要进行修改。
4.  执行akskOcrService函数，控制台输出200即表示程序执行成功。身份证服务的结果可以采用json编辑器展示。

    ```
    {
        "result": {
            "name": "李蓝", 
            "sex": "女", 
            "ethnicity": "满", 
            "birth": "1990-01-24", 
            "address": "河北省承德市围场满族蒙古族自治县金车路", 
            "number": "389201199001245580"
        }
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >如想调用OCR其他识别服务，只需要把akskOcrService函数的“uri”参数改成对应的URI即可。URI列表请参见[表1 接口与API对应关系表](文字识别SDK简介.md#table47650414583)。  


## Token认证方式<a name="section10576225195619"></a>

本节以身份证识别服务为例介绍如何以Token认证方式使用SDK。

1.  打开ViewController.m文件，修改tokenOcrService函数中的username、password和domainName为系统中实际注册的用户名、密码和账号名（如果用户为非IAM用户，账号名与用户名一致），请参见[图2](#fig41868318)。

    **图 2**  修改ViewController.m文件中的用户名、密码和账号名<a name="fig41868318"></a>  
    ![](figures/修改ViewController-m文件中的用户名-密码和账号名.png "修改ViewController-m文件中的用户名-密码和账号名")

2.  直接执行相应代码，在控制台可看到使用Token方式身份证识别服务的识别结果。

