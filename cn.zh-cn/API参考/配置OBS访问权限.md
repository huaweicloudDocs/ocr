# 配置OBS访问权限<a name="ocr_03_0132"></a>

EI企业智能服务对于图片、语音等多媒体文件支持直接使用OBS服务的数据处理方式，以减少服务使用成本，降低服务的响应时长，提升服务使用的体验。

考虑到数据的安全，当对服务进行授权后，才可以使用授权方式的URL（https://<bucket-name\>.<endpoint\>/<object-name\>）对服务进行访问。若未对服务授权，则无法直接获取到用户数据，需要用户开启公共读授权或者提供一个临时授权的URL。

## 对文字识别服务开启授权<a name="section3969614172019"></a>

如果您需要使用OBS中的数据，请开通对象存储服务OBS授权。进入[文字识别OCR主页](https://www.huaweicloud.com/product/ocr.html)，单击“立即使用“，进入文字识别控制台（需要使用华为云账号登录）。单击“服务管理“页面，打开对象存储服务OBS授权的按钮，完成授权操作。完成授权即可使用授权方式的URL对服务进行访问。

**图 1**  OBS授权<a name="fig152684128246"></a>  
![](figures/OBS授权.png "OBS授权")

>![](public_sys-resources/icon-note.gif) **说明：** 
>不支持跨区域OBS，OBS的区域需要和服务保持一致。

## 开启公共读授权<a name="section788312305717"></a>

若需要开启公共读授权，可以参见《对象存储服务控制台指南》[“权限控制”](https://support.huaweicloud.com/usermanual-obs/obs_03_0086.html)章节中的相关内容，完成桶的ACL权限配置。完成设置，在OBS服务上传完相应的文件后，即可通过URL访问OBS上的数据。也可将该URL作为EI企业智能服务的API请求参数，使用相关的服务接口。

## 使用临时授权请求鉴权<a name="section82216406330"></a>

开启公共读授权访问，虽然使用比较方便，但若对于敏感的信息，例如个人的私有数据，存在泄露风险。此场景下，可以考虑OBS提供的临时授权功能。

OBS服务支持用户对OBS服务中的对象构造一个特定URL，URL中会包含鉴权信息，任何用户都可以通过该URL访问OBS中的对象，但该URL只在Expires指定的失效时间内有效。该方式用于在不提供给其他人Secret Access Key的情况下，让其他人能够执行自己定义的操作。

进一步了解和使用OBS临时授权功能，请参见[《对象存储服务SDK参考》](https://support.huaweicloud.com/sdkreference-obs/obs_02_0001.html)对应语言的“授权访问”章节的相关内容，下载相关的SDK及示例代码，并进行相关的编码开发，以支持相关的URL获取。

