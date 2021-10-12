# Python SDK<a name="ocr_04_0026"></a>

用户使用服务的认证方式有Token和AK/SK两种，获取认证消息请参考[认证鉴权](https://support.huaweicloud.com/api-ocr/ocr_03_0005.html)。本章节主要包含Token和AK/SK两种方式使用SDK进行示例说明。

下载[OCR Python SDK开发工具包](https://mirrors.huaweicloud.com/mirrors_sdk/ocr-sdk/ocr-python-sdk/cloud-ocr-sdk-python-1.0.7.rar)。

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   SDK中涉及到的所有图像均为合成的非真实图像，仅供示例参考使用。
>-   用户首次使用需要先[申请开通](https://console.huaweicloud.com/ocr/?region=cn-north-4&locale=zh-cn#/ocr/management/main)该服务。服务只需要开通一次即可，后面使用时无需再次申请。如未开通服务，调用服务时会提示ModelArts.4204报错，请在调用服务前先进入控制台开通服务，并注意开通服务区域与调用服务的区域保持一致。

## AK/SK认证方式<a name="section20574102575613"></a>

本节以身份证别服务为例介绍如何以AK/SK认证方式使用SDK。

1.  获取AK/SK，具体步骤请参见[认证鉴权\>AK/SK认证](https://support.huaweicloud.com/api-ocr/ocr_03_0005.html#section1)。
2.  配置Python SDK的AK/SK。

    根据获取的AK/SK，修改Demo工程“OCRDemo.py”文件中aksk\_request函数的“AK”和“SK”的值。

    **图 1**  修改OCRDemo.py文件参数<a name="fig13342818339"></a>  
    ![](figures/修改OCRDemo-py文件参数.png "修改OCRDemo-py文件参数")

3.  修改输入参数。

    如使用本地图片文件进行识别，修改OCRDemo.py文件参数“img\_path”为本地图片路径。如使用SDK默认图片则不需要进行修改。

4.  执行OCRDemo.py文件，控制台输出200即表示程序执行成功。在控制台可以查看身份证的结果。

    ```
    {
        "result": {
            "name": "xx", 
            "sex": "女", 
            "ethnicity": "满", 
            "birth": "1990-xx-xx", 
            "address": "河北省承德市围场满族蒙古族自治县金车路", 
            "number": "3892011990012xxxxx"
        }
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >如想调用OCR其他识别服务，只需要把aksk\_request函数的"req\_uri"参数改成对应的URI即可。URI列表请参见[表1 接口与API对应关系表](文字识别SDK简介.md#table47650414583)。


## Token认证方式<a name="section10576225195619"></a>

本节以身份证识别服务为例介绍如何以Token认证方式使用SDK。

1.  打开OCRDemo.py文件，修改token\_request函数中的username、password和domain\_name为系统中实际注册的用户名、密码和账号名（如果用户为非IAM用户，账号名与用户名一致）。

    **图 2**  修改OCRDemo.py文件中的用户名、密码和账号名<a name="fig55543468"></a>  
    ![](figures/修改OCRDemo-py文件中的用户名-密码和账号名.png "修改OCRDemo-py文件中的用户名-密码和账号名")

2.  直接执行相应代码，在控制台可看到使用Token方式身份证识别服务的识别结果。

## 状态码<a name="zh-cn_topic_0085429345_section59700980145140"></a>

状态码请参见[状态码](https://support.huaweicloud.com/api-ocr/ocr_03_0090.html)。

## 错误码<a name="section545533743312"></a>

错误码请参见[错误码](https://support.huaweicloud.com/api-ocr/ocr_03_0028.html)。

