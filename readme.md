# API地址

    https://api-shoushou.shenmayouxi.com/  

-----

## 说明
初次写接口文档，格式不好请见谅。  
  
本接口为根接口。  
支付逻辑方面未知。  
具体用法请参考以下文件：  
  
[BootStrapper](bootstrapper.md)  
- 启动验证接口
  - *--没有次级接口--*

[Good](good.md)  
- 点赞相关接口
  - unread / 获取未读消息数目(小红点)
  - received / "赞我的毛毛"
  - medo / "我赞的毛毛"
  - doo / "毛毛之家"点赞

[Account](account.md)  
- 用户相关接口
  - smscaptcha / 短信发送接口
  - smsloginregister / 用户验证接口

[Fursona](fursona.md)  
- 捏兽相关接口
  - has / 捏兽数据查重
  - nameCheck / 设定名称查重
  - my / 我的设定(仅服务器端/"已保护")
  - room / "毛毛之家"
  - new / "上传捏兽"? 疑似存在，未捕捉到
  - renew / "续费捏兽"? 疑似存在，未捕捉到
  - remove / "移除捏兽"? 疑似存在，未捕捉到

-----

## Headers
这是应用内发出HTTPS时使用的Headers，测试后发现某些情况下也可不使用这个Headers  
```
Host: api-shoushou.shenmayouxi.com
Content-Type: application/x-www-form-urlencoded
User-Agent: shoushou/1 CFNetwork/1220.1 Darwin/20.3.0
Accept: */*
Accept-Language: zh-cn
Accept-Encoding: gzip, deflate, br
X-Unity-Version: 2019.3.13f1
```

-----

## token相关
本应用的绝大多数次级接口都是需要带token访问的。  
token可以在**用户验证接口**处获得  
token形式上为base64字符串(此处为例子)  
```
eyJpZCI6MCwiYXBwIjoic2hvdXNob3UiLCJ0aW1lIjowfQ==
```
解密后为json字符串  
为去除了多余空格和换行符等内容的格式  
```json
{"id":0,"app":"shoushou","time":0}
```
格式化后:  
```json
{
    "id":0,
    "app":"shoushou",
    "time":0
}
```
| Key | Type | Description |
| --- | ---- | ----------- |
| id  | int  | 用户id      |
| app | str  | 固定值"shoushou" |
| time | int | (推测)注册时间 |

    以上的(int)0均为占位符
