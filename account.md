# API地址

    https://api-shoushou.shenmayouxi.com/account/  

## 说明
本接口为用户登录相关的接口, 已经明确的次级接口有
- smscaptcha / 短信发送接口
- smsloginregister / 用户验证接口

本应用没有真正意义的退出登录, 退出登录只是删除存储在本机上的token  

-----

# smscaptcha / 短信发送接口

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/account/smscaptcha

## 说明
本次级接口用于申请向手机号发送短信, 左上角用户登录时点击发送短信会调用1次。  
服务器端设置了60秒的时间限制, 即60秒内对同一手机号只能发送一次短信。  

## 请求
请求方式: *POST*  
*可选携带Headers*  
请求参数(body):  
| Key | Type | Description |
| --- | ---- | ----------- |
| phone | int | 手机号 |

## 响应
| Key | Type | Description |
| --- | ---- | ----------- |
| code | str | 状态码 |
| msg | str | 状态码对应的具体内容 |
| data | dict | (视情况可能没有data键) |

```json
{
  "code": "200",
  "msg": "操作成功",
  "data": {}
}
```

-----

# smsloginregister / 用户验证接口

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/account/smsloginregister

## 说明
本次级接口用于将手机号收到的验证码上传到服务器进行验证，验证成功后返回用户数据。  
手机的验证码有效期为5分钟。  

## 请求
请求方式: *POST*  
*可选携带Headers*  
请求参数(body):  
| Key | Type | Description |
| --- | ---- | ----------- |
| phone | int/str | 手机号 |
| captcha | int/str | 六位数验证码 |

## 响应
| Key | Type | Description |
| --- | ---- | ----------- |
| code | str | 状态码 |
| msg | str | 状态码对应的具体内容 |
| data | dict | (视情况可能没有data键) |

### data中的内容

| Key | Type | Description |
| --- | ---- | ----------- |
| id | int/str | 用户id |
| name | str | 用户昵称 |
| bgColor | str | (推测)不知用于何处的背景颜色 |
| roomId | int/str | 房间背景图 |
| icon | str | (推测)设定图 |
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