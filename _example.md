# 接口名称或次级接口名称

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/...


## 说明
本接口用于……  

## 请求
请求方式: *POST*  
*可选携带Headers*  
请求参数(body):  
| Key | Type | Description |
| --- | ---- | ----------- |
| token | base64/str | 令牌 |
| ... | ... | ... |

## 响应
| Key | Type | Description |
| --- | ---- | ----------- |
| code | str | 状态码 |
| msg | str | 状态码对应的具体内容 |
| data | dict | (视情况可能没有data键) |

### data中的内容

| Key | Type | Description |
| --- | ---- | ----------- |
| ... | ... | ... |

```json
{
  "code": "200",
  "msg": "操作成功",
  "data": {
    "...": 0
  }
}
```