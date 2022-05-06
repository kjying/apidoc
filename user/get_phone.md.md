### 阿里云快速登录获取手机号

##### HTTP Method: GET
##### URL: https://host/app/user/get_phone.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
access_token|string|阿里云token|true| 
imei|string||否|


* 如获取到手机号, 返回用户id. id>0为用户已存在, 客户端登录.id=0客户端注册.
* 如获取到手机号, 返回验证码, 用户不用再获取和输入验证码.
* iOS手机号未注册, imei已注册, 此时自动绑定手机号并返回对应用户id

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "phone": "123456789",
        "id": 1,
        "rand": 1111,
    },
    "desc": ""
}
```

##### HTTP Response error
```json
{
    "code": 401,
    "data": "",
    "desc": "获取手机号失败"
}
```


