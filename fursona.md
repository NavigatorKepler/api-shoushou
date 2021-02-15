# API地址

    https://api-shoushou.shenmayouxi.com/fursona/  

## 说明
本接口为捏兽相关内容的接口，已经明确的次级接口有  
- has / 捏兽数据查重
- nameCheck / 设定名称查重
- my / 我的设定(仅服务器端/"已保护")
- room / "毛毛之家"

用法尚不明确的接口有  
- new / "上传捏兽"?
- renew / "续费捏兽"?
- remove / "移除捏兽"?

-----

# has / 捏兽数据查重

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/fursona/has

## 说明
本接口用于在此平台内查询捏兽数据是否有重复，正常情况下会在捏兽完成时调用1次。  

## 请求
请求方式: *POST*  
*可选携带Headers*  
请求参数(body):  
| Key | Type | Description |
| --- | ---- | ----------- |
| token | base64/str | 令牌 |
| content | str | 捏兽数据(长数据) |

content示例内容如下  
*注: 可以按照大型存档理解此处的数据*  
```
脸/1,头发/空,耳朵/1,眼睛/1,嘴/1,眉毛/1,犄角/空,手/1,尾巴/1,身材/1,脚/1,翅膀/空,头花纹/空,身体花纹/空,眼镜/空,帽子/空,上衣/空,领带/空,裤子/空,面具/空,上衣_1_Single_color/ffd3ca,上衣_2_Single_color/ffdf86,上衣_3_Single_color/a7ffd1,嘴_1_Single_color/f6c87a,嘴_2_Single_color/f6c87a,嘴_3_Single_color/f6c87a,嘴_4_Single_color/f6c87a,嘴_5_Single_color/f6c87a,嘴_6_Single_color/f6c87a,嘴_7_Single_color/f6c87a,嘴_8_Single_color/f6c87a,嘴_9_Single_color/f6c87a,头花纹_1_Single_color/dd7c61,头花纹_2_Single_color/dd7c61,头花纹_3_Single_color/dd7c61,头花纹_4_Single_color/dd7c61,头花纹_5_Single_color/a787b9,头花纹_6_Single_color/92a6d5,头花纹_7_Single_color/ffffff,头花纹_8_Single_color/bd8982,头花纹_9_Single_color/d3454a,头花纹_10_Single_color/a7e1db,头花纹_11_Single_color/ffffff,头花纹_12_Single_color/d3454a,头花纹_13_Single_color/d09f77,头花纹_14_Single_color/c2a996,头花纹_15_Single_color/dd7c61,头花纹_16_Single_color/c3d3bb,头花纹_17_Single_color/bd8982,头花纹_18_Single_color/c1d8e2,尾巴_1_Single_color/f6c87a,尾巴_2_Single_color/f6c87a,尾巴_3_Single_color/f6c87a,尾巴_4_Single_color/f6c87a,尾巴_5_Single_color/f6c87a,尾巴_6_Single_color/f6c87a,尾巴_7_Single_color/f6c87a,尾巴_8_Single_color/f6c87a,尾巴_9_Single_color/f6c87a,尾巴_10_Single_color/f6c87a,帽子_1_Single_color/628de0,帽子_2_Single_color/628de0,帽子_3_Single_color/ffd3ca,手_1_Single_color/f6c87a,手_2_Single_color/f6c87a,手_3_Single_color/f6c87a,手_4_Single_color/f6c87a,手_5_Single_color/ffffff,手_6_Single_color/f6c87a,眉毛_1_Single_color/5f1c1f,眉毛_2_Single_color/ffffff,眉毛_3_Single_color/f6c87a,眉毛_4_Single_color/d3454a,眉毛_5_Single_color/a787b9,眉毛_6_Single_color/c1d8e2,眉毛_7_Single_color/c1d8e2,眉毛_8_Single_color/ffffff,眼睛_1_Single_color/ffd3ca,眼睛_2_Single_color/ffd3ca,眼睛_3_Single_color/ffd3ca,眼睛_4_Single_color/d3454a,眼睛_5_Single_color/d3454a,眼睛_6_Single_color/d3454a,眼睛_7_Single_color/d3454a,眼睛_8_Single_color/d3454a,眼镜_1_Single_color/628de0,眼镜_2_Single_color/ffdf86,眼镜_3_Single_color/ffdf86,眼镜_4_Single_color/a7e1db,眼镜_5_Single_color/92a6d5,眼镜_6_Single_color/c1d8e2,翅膀_1_Single_color/ffccf1,翅膀_2_翼骨_color/628de0,翅膀_2_翼膜_color/ffccf1,翅膀_3_Single_color/628de0,翅膀_4_Single_color/c1d8e2,翅膀_5_Single_color/92a6d5,翅膀_6_Single_color/a7e1db,翅膀_7_Single_color/d3454a,翅膀_8_Single_color/f6c87a,耳朵_1_Single_color/f6c87a,耳朵_2_Single_color/f6c87a,耳朵_3_Single_color/f6c87a,耳朵_4_Single_color/f6c87a,耳朵_5_Single_color/f6c87a,耳朵_6_Single_color/f6c87a,耳朵_7_Single_color/f6c87a,耳朵_8_Single_color/f6c87a,耳朵_9_Single_color/f6c87a,耳朵_10_Single_color/f6c87a,耳朵_11_Single_color/f6c87a,脚_1_Single_color/f6c87a,脚_2_Single_color/f6c87a,脚_3_Single_color/f6c87a,脚_4_Single_color/f6c87a,脚_5_Single_color/f6c87a,脚_6_Single_color/f6c87a,脸_1_Single_color/f6c87a,脸_2_Single_color/f6c87a,裤子_1_Single_color/628de0,裤子_2_Single_color/628de0,裤子_3_Single_color/628de0,身材_1_Single_color/f6c87a,身材_2_Single_color/f6c87a,身材_3_Single_color/f6c87a,身材_4_Single_color/f6c87a,领带_1_Single_color/628de0,领带_2_Single_color/e7d0ff,领带_3_Single_color/9effde,领带_4_Single_color/d3454a,领带_5_Single_color/d3454a,领带_6_Single_color/a787b9,领带_7_Single_color/92a6d5,领带_8_Single_color/889f6a,身体花纹_1_Single_color/dd7c61,身体花纹_2_Single_color/dd7c61,身体花纹_3_Single_color/dd7c61,身体花纹_4_Single_color/dd7c61,身体花纹_5_Single_color/a787b9,身体花纹_6_Single_color/92a6d5,身体花纹_7_Single_color/ffffff,身体花纹_8_Single_color/bd8982,身体花纹_9_Single_color/d3454a,身体花纹_10_Single_color/623d28,身体花纹_11_Single_color/ffffff,身体花纹_12_Single_color/ee9dae,身体花纹_13_Single_color/92a6d5,身体花纹_14_Single_color/5f1c1f,身体花纹_15_Single_color/dd7c61,身体花纹_16_Single_color/2a3f4a,身体花纹_17_Single_color/d3454a,身体花纹_18_Single_color/c1d8e2,头发_1_Single_color/ffffff,头发_2_Single_color/ffffff,头发_3_Single_color/ffffff,头发_4_Single_color/ffffff,头发_5_Single_color/ffffff,犄角_1_Single_color/9d2832,犄角_2_Single_color/d3454a,犄角_3_Single_color/f6c87a,犄角_4_Single_color/c3d3bb,犄角_5_Single_color/a7e1db,犄角_6_Single_color/c2a996,犄角_7_Single_color/d09f77,犄角_8_Single_color/a7e1db,犄角_9_Single_color/a7e1db,犄角_10_Single_color/a787b9,犄角_11_Single_color/a7e1db,犄角_12_Single_color/5f1c1f,犄角_13_Single_color/a7e1db,犄角_14_Single_color/ee9dae,犄角_15_Single_color/c3d3bb,犄角_16_Single_color/c3d3bb,犄角_17_Single_color/c3d3bb,犄角_18_Single_color/a7e1db,犄角_19_Single_color/c3d3bb,犄角_20_Single_color/a7e1db,面具_1_Single_color/e8d088,面具_2_Single_color/d3454a,面具_3_Single_color/d3454a,面具_4_Single_color/5f1c1f,面具_5_Single_color/e8d088,面具_6_Single_color/ffffff,面具_7_Single_color/ffffff,面具_8_Single_color/ee9dae,面具_9_Single_color/ffffff,面具_10_Single_color/ffffff
```

## 响应
| Key | Type | Description |
| --- | ---- | ----------- |
| code | str | 状态码 |
| msg | str | 状态码对应的具体内容 |
| data | dict | (视情况可能没有data键) |

### data中的内容

| Key | Type | Description |
| --- | ---- | ----------- |
| canUse | bool | 捏兽角色可用性 |

```json
{
  "code": "200",
  "msg": "操作成功",
  "data": {
    "canUse": false
  }
}
```

-----

# nameCheck / 设定名称查重

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/fursona/nameCheck

## 说明
本接口用于在此平台内查询设定名称是否有重复, 正常情况下在输入角色昵称时会调用1次。  

## 请求
请求方式: *POST*  
*可选携带Headers*  
请求参数(body):  
| Key | Type | Description |
| --- | ---- | ----------- |
| token | base64/str | 令牌 |
| name | str | 角色昵称 |

## 响应
| Key | Type | Description |
| --- | ---- | ----------- |
| code | str | 状态码 |
| msg | str | 状态码对应的具体内容 |
| data | dict | (视情况可能没有data键) |

### data中的内容

| Key | Type | Description |
| --- | ---- | ----------- |
| canUse | bool | 角色昵称可用性 |

```json
{
  "code": "200",
  "msg": "操作成功",
  "data": {
    "canUse": true
  }
}
```

-----

# my / 我的设定(仅服务器端/"已保护")

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/fursona/my

## 说明
本接口用于从平台上获取已经上传的捏兽数据, 正常情况下应当会在每次回到首页时调用(或者启动时调用, 调用机制暂不明)1次  

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
| canUse | bool | 角色昵称可用性 |

```json
{
  "code": "200",
  "msg": "操作成功",
  "data": {
    "canUse": true
  }
}
```

-----

# room / "毛毛之家"

## 次级接口地址

    https://api-shoushou.shenmayouxi.com/fursona/room

## 说明
本接口用于从平台上获取"毛毛之家"页面的数据  

## 请求
请求方式: *POST*  
*可选携带Headers*  
请求参数(body):  
| Key | Type | Description |
| --- | ---- | ----------- |
| token | base64/str | 令牌 |
| page | int | 页码 |

## 响应
| Key | Type | Description |
| --- | ---- | ----------- |
| code | str | 状态码 |
| msg | str | 状态码对应的具体内容 |
| data | dict | (视情况可能没有data键) |

### data中的内容

| Key | Type | Description |
| --- | ---- | ----------- |
| sum | int | (推测)房间总数 |
| list | list | (视情况可能为空列表)房间列表 |
| page | int | 指示当前的页码 |

### list中每个元素的内容(即描述每个房间特征的数据)

| Key | Type | Description |
| --- | ---- | ----------- |
| id | int/str | 用户id |
| name | str | 用户昵称 |
| roomId | int/str | 房间背景图 |
| fursonas | list | (视情况可能为空列表)此房间中的设定列表 |

### fursonas中每个元素的内容(即描述每个设定特征的数据)

| Key | Type | Description |
| --- | ---- | ----------- |
| userid | int/str | 用户id |
| id | int/str | 设定id |
| name | str | 设定名称 |
| icon | str | 生成的设定图片(小图) |
| bgColor | HEX/str | (推测)不知用于何处的背景颜色 |
| created | int/str | 创建时间戳 |
| expireDate | YYYY-MM-DD/str | (推测)"设定保护"到期时间 |
| isLocking | int/str | 指示是否正在保护(一般来说, 能看到的都是正在保护的) |
| goodNumber | int/str | 点赞数 |
| iconBig | str | 生成的设定图片(大图) |
| isMyGood | bool | 指示自己是否曾经赞过 |

*为节省篇幅，此范例有省略*  
```json
{
  "code": "200",
  "msg": "操作成功",
  "data": {
    "sum": 47,
    "list": [
      {
        "id": "10030",
        "name": "456",
        "roomId": "3",
        "fursonas": [
          {
            "userId": "10030",
            "id": "10027",
            "name": "456",
            "icon": "https://cdn.shenmayouxi.com/shoushou/upfs/202102/07/1080w1920hf_1612694274121732.png!270x480.jpg",
            "bgColor": "FFFFFF",
            "created": "1612694274",
            "expireDate": "2021-03-09",
            "isLocking": "1",
            "goodNumber": "21",
            "iconBig": "https://cdn.shenmayouxi.com/shoushou/upfs/202102/07/1080w1920hf_1612694274121732.png",
            "isMyGood": false
          }
        ]
      },
      {
        "id": "10115",
        "name": "知安",
        "roomId": "2",
        "fursonas": [
          {
            "userId": "10115",
            "id": "10068",
            "name": "知安",
            "icon": "https://cdn.shenmayouxi.com/shoushou/upfs/202102/14/1080w1920hf_1613274382920408.png!270x480.jpg",
            "bgColor": "FFFFFF",
            "created": "1613274383",
            "expireDate": "2021-03-16",
            "isLocking": "1",
            "goodNumber": "12",
            "iconBig": "https://cdn.shenmayouxi.com/shoushou/upfs/202102/14/1080w1920hf_1613274382920408.png",
            "isMyGood": false
          }
        ]
      }
    ],
    "page": 1
  }
}
```