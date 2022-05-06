### 用户手机、微信号绑定、Facebook绑定、Google绑定接口

##### HTTP Method: POST
##### URL: https://host/app/user/phone_verify.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid        |int| |true|   
session_id  |int| |true| 
type|int| 类型 1绑定手机号码 2绑定微信号(旧) 3绑定微信号 4Facebook 5Google|true|1
phone          |  string | 手机号|true|
authcode       |  string | 短信验证码|true|
token |  string | 微信openid、Facebook唯一标识码、Google唯一标识码|true|
##### HTTP Response
```json
{
    "code": 200,//400 错误
    "data": {
        "result": 1,//2 用户未登陆
        "msg": {   //用户基本信息，字段含义参考之前的接口
            "id": "1044",
            "nickname": "legolas",
            "head_image": "https://api.iofol.cn/public/upload/head_image/2016-05-19/1044-1463639583.jpg",
            "weixinId": "",  //openid，微信用户的唯一标识，也可以用来判断是否绑定微信号
            "signature": "",
            "phone": "13794305519",
            "sex": "1",
            "age": "36",
            "session_id": "38c1719f1560b5a7c555d2b81f128d8b",
            "login_time": "1463639882",
            "register_ip": "192.168.0.141",
            "register_time": "1463639263",
            "imei": "muyou",
            "is_binding": "1",
            "isdel": "0",
            "vip": "0",
            "height": "188",
            "weixin": "",
            "qq": "",
            "income": "3",
            "marry": "1",
            "province": "",
            "city": "",
            "user_type": "0",
            "version_code": "muyou",
            "ext": {
                "job": "3",
                "education": "3",
                "birthday": "",
                "weight": "",
                "constellation": "",
                "bust": "D"  //胸围罩杯
            },
            "channel": "",
            "head_image_status": "1",
            "qq_show": "0",
            "phone_show": "0",
            "weixin_show": "0",
            "online": "1",
            "vip_buy_type": "2",  // 1: vip月卡   2：vip季度卡(季度vip)
            "facebookId": "",
            "googleId": "",
        }
    },
    "desc": "验证成功"
}
```