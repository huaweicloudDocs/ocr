# 获取项目ID<a name="ocr_03_0130"></a>

## 从控制台获取项目ID<a name="section19885123154616"></a>

1.  登录[管理控制台](https://console.huaweicloud.com/console/?locale=zh-cn)。
2.  鼠标移动到右上角的用户名上，在下拉列表中选择“我的凭证“。
3.  在“我的凭证“页面，可以查看用户名、账号名，在项目列表中查看项目。

    **图 1**  查看项目ID<a name="fig20626132135515"></a>  
    ![](figures/查看项目ID.png "查看项目ID")

    多项目时，展开“所属区域“，从“项目ID“列获取子项目ID。


## 调用API获取项目ID<a name="section152741133194610"></a>

获取项目ID的接口为“GET https://\{endpoint\}/v3/projects“，其中“\{endpoint\}“为IAM的终端节点。接口的认证鉴权请参见[认证鉴权](认证鉴权.md)。

响应示例如下，例如，文字识别服务部署的区域为“cn-north-4“，响应消息体中查找“name“为“cn-north-4“，其中“projects“下的“id“即为项目ID。

```
{ 
    "projects": [ 
        { 
            "domain_id": "65382450e8f64ac0870cd180d14e684b", 
            "is_domain": false, 
            "parent_id": "65382450e8f64ac0870cd180d14e684b", 
            "name": "project_name", 
            "description": "", 
            "links": { 
                "next": null, 
                "previous": null, 
                "self": "https://www.example.com/v3/projects/a4a5d4098fb4474fa22" 
            }, 
            "id": "a4a5d4098fb4474fa22cd05f897d6b99", 
            "enabled": true 
        } 
    ], 
    "links": { 
        "next": null, 
        "previous": null, 
        "self": "https://www.example.com/v3/projects" 
    } 
}
```

