# API地址

    https://api-shoushou.shenmayouxi.com/  

-----
# 说明
本接口为根站点。  
具体用法请参考以下文件：  
[BootStrapper](bootstrapper.md)  
- 启动验证

[Good / ？](good.md)  

[Account / 用户相关](account.md)  
- 短信发送
- 用户验证

[Fursona / 设定相关](fursona.md)  


# Headers
```
Host: api-shoushou.shenmayouxi.com
Content-Type: application/x-www-form-urlencoded
User-Agent: shoushou/1 CFNetwork/1220.1 Darwin/20.3.0
Accept: */*
Accept-Language: zh-cn
Accept-Encoding: gzip, deflate, br
X-Unity-Version: 2019.3.13f1
```

# token相关
该接口的绝大多数次级接口都是需要带token访问的。  
token形式上为base64字符串(此处为例子)  
'''
eyJpZCI6MCwiYXBwIjoic2hvdXNob3UiLCJ0aW1lIjowfQ==
'''
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
