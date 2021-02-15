# API地址

    https://api-shoushou.shenmayouxi.com/account  

-----
## 说明
本接口下设smscaptcha和smsloginregister两个次级接口  

# smscaptcha / 短信发送接口

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/account/smscaptcha

## 说明
本次级接口用于申请向手机号发送短信  

## 请求
请求方式: *POST*  
*必须携带Headers*  
请求参数:  
| Key | Type | Description |
| --- | ---- | ----------- |
| phone | int | 手机号 |

## 响应
| Key | Type | Description |
| --- | ---- | ----------- |
| code | str | 状态码 |
| msg | str | 状态码对应的具体内容 |
| data | dict | -- |

```json
{
  "code": "200",
  "msg": "操作成功",
  "data": {}
}
```

# smsloginregister / 用户验证接口

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/account/smsloginregister

## 说明
本次级接口用于将手机号收到的验证码上传到服务器进行验证，并获取用户数据。  

## 请求
请求方式: *POST*  
*必须携带Headers*  
请求参数:  
| Key | Type | Description |
| --- | ---- | ----------- |
| phone | int/str | 手机号 |
| captcha | int/str | 六位数验证码 |

## 响应
| Key | Type | Description |
| --- | ---- | ----------- |
| code | str | 状态码 |
| msg | str | 状态码对应的具体内容 |
| data | dict | -- |

### data中的内容

| Key | Type | Description |
| --- | ---- | ----------- |
| id | int/str | 用户id |
| name | str | 用户昵称 |
| bgColor | str | (字面意义)界面背景色 |
| roomId | int/str | 房间背景图 |
| icon | str | (不知用于何处的)图标 |
| token | base64/str | 令牌 |

```json
{
  "code": "200",
  "msg": "操作成功",
  "data": {
    "id": 0,
    "name": "小动物",
    "bgColor": "",
    "roomId": "5",
    "icon": "",
    "token": 0
  }
}
```

    以上的(int)0均为占位符