# API地址

    https://api-shoushou.shenmayouxi.com/bootstrapper  

-----

## 说明
本接口会在应用启动时带token访问一次。  
(推测)本接口用于刷新当前记录的令牌，并获取用户基本信息。  

## 请求
请求方式: *POST*  
*可选携带Headers*  
请求参数(body):  
| Key | Type | Description |
| --- | ---- | ----------- |
| token | base64/str | 令牌 |

## 响应

| Key | Type | Description |
| --- | ---- | ----------- |
| code | int/str | 状态码 |
| msg | str | 状态码对应的具体内容 |
| data | dict | (视情况可能没有data键) |

### data中的内容

| Key | Type | Description |
| --- | ---- | ----------- |
| defaultName | str | 默认昵称 |
| defaultIcon | str | 默认头像 |
| version | str | 版本号 |
| versionNumber | int/str | 版本号对应的编号 |

```json
{
  "code": "200",
  "msg": "操作成功",
  "data": {
    "defaultName": "小动物",
    "defaultIcon": "",
    "version": "1.00",
    "versionNumber": "100"
  }
}
```
