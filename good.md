# API地址

    https://api-shoushou.shenmayouxi.com/good  

## 说明
本接口为点赞相关内容的接口，已经明确的次级接口有  
- unread / 获取未读消息数目(小红点)
- doo / "毛毛之家"点赞
- medo / "我赞的毛毛"

用法尚不完善的接口有  
- received / "赞我的毛毛"

-----

# unread / 获取未读消息数目(小红点)

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/good/unread

## 说明
本接口用于获取未读点赞数目(相当于小红点)  

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
| code | str | 状态码 |
| msg | str | 状态码对应的具体内容 |
| data | dict | (视情况可能没有data键) |

### data中的内容

| Key | Type | Description |
| --- | ---- | ----------- |
| number | int/str | 小红点数目 |

```json
{
  "code": "200",
  "msg": "操作成功",
  "data": {
    "number": "0"
  }
}
```

-----

# doo / "毛毛之家"点赞

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/good/doo

## 说明
本接口用于进行点赞操作  

## 请求
请求方式: *POST*  
*可选携带Headers*  
请求参数(body):  
| Key | Type | Description |
| --- | ---- | ----------- |
| token | base64/str | 令牌 |
| fursonaId | int | (同"毛毛之家"中的)设定id |
| type | int\|\|str | *意义暂时不明*可以任意取值, 也可留空 |

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

# received / "赞我的毛毛"

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/good/received

## 说明
本接口用于获取"赞我的毛毛"  

## 请求
请求方式: *POST*  
*可选携带Headers*  
请求参数(body):  
| Key | Type | Description |
| --- | ---- | ----------- |
| token | base64/str | 令牌 |
| page | int/str | 指示需要的页面 |

## 响应
| Key | Type | Description |
| --- | ---- | ----------- |
| code | str | 状态码 |
| msg | str | 状态码对应的具体内容 |
| data | dict | (视情况可能没有data键) |

### data中的内容

| Key | Type | Description |
| --- | ---- | ----------- |
| sum | int | 赞我的总数 |
| page | int | 指示当前的页码 |
| list | list | (视情况可能为空列表)因为拿到了空列表无法进一步分析 |


```json
{
  "code": "200",
  "msg": "操作成功",
  "data": {
    "sum": 1,
    "page": 1,
    "list": []
  }
}
```

-----

# medo / "我赞的毛毛"

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/good/medo

## 说明
本接口用于获取"我赞的毛毛"  

## 请求
请求方式: *POST*  
*可选携带Headers*  
请求参数(body):  
| Key | Type | Description |
| --- | ---- | ----------- |
| token | base64/str | 令牌 |
| page | int/str | 指示需要的页面 |

## 响应
| Key | Type | Description |
| --- | ---- | ----------- |
| code | str | 状态码 |
| msg | str | 状态码对应的具体内容 |
| data | dict | (视情况可能没有data键) |

### data中的内容

| Key | Type | Description |
| --- | ---- | ----------- |
| sum | int | 我赞的总数 |
| page | int | 指示当前的页码 |
| list | list | (视情况可能为空列表)我赞的列表 |

### list中的内容(即我赞的列表中的内容)

| Key | Type | Description |
| --- | ---- | ----------- |
| id | int/str | (疑似)点赞编号 |
| name | str | 点赞对象的昵称 |
| icon | str | 生成的设定图片(小图) |
| bgColor | HEX/str | (推测)不知用于何处的背景颜色 |
| expireDate | YYYY-MM-DD/str | (推测)"设定保护"到期时间 |
| isLocking | int/str | 指示是否正在保护(一般来说, 能看到的都是正在保护的) |
| iconBig | str | 生成的设定图片(大图) |
| created | int | 点赞时间戳 |

```json
{
  "code": "200",
  "msg": "操作成功",
  "data": {
    "sum": 2,
    "list": [
      {
        "id": "1210",
        "name": "林小黑",
        "icon": "https://cdn.shenmayouxi.com/shoushou/upfs/202102/14/1080w1920hf_1613289780887209.png!270x480.jpg",
        "bgColor": "FFFFFF",
        "expireDate": "2021-03-16",
        "isLocking": "1",
        "iconBig": "https://cdn.shenmayouxi.com/shoushou/upfs/202102/14/1080w1920hf_1613289780887209.png",
        "created": "1613376906"
      },
      {
        "id": "1209",
        "name": "456",
        "icon": "https://cdn.shenmayouxi.com/shoushou/upfs/202102/07/1080w1920hf_1612694274121732.png!270x480.jpg",
        "bgColor": "FFFFFF",
        "expireDate": "2021-03-09",
        "isLocking": "1",
        "iconBig": "https://cdn.shenmayouxi.com/shoushou/upfs/202102/07/1080w1920hf_1612694274121732.png",
        "created": "1613376900"
      }
    ],
    "page": 1
  }
}
```