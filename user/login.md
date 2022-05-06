### 用户登录

##### HTTP Method: POST
##### URL: https://host/app/user/login.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid          |int| 账号 |true|       
password     |string| 密码 |true|
version_code |int|| app版本号|true|
package |string|包名|true|
imei         |string|imei|true|
phone |string|手机号码|false|
phone_code |string|手机号登录验证码|false|
token         |string|微信openid、Facebook、Google|false|
channel |string| 渠道号|true|
type         |int|登陆类型 0 账号密码登陆 1 快速登陆 2手机号码登录 3微信登录 4Facebook登录 5Google登录|true|0

"result": 1,  //1 登录成功，2 账号或密码错误，4 资料未完善(需要跳转到完善资料页面) 6 该设备或该手机号或该微信号没有注册过账号 7.190版本女性未实名验证 8 270版本男性用户未选择标签

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,  //1 登录成功，2 账号或密码错误，4 资料未完善(需要跳转到完善资料页面) 6 该设备或该手机号或该微信号没有注册过账号 7.190版本女性未实名验证 8 270版本男性用户未选择标签
        "msg": {    //字段说明请看session接口
            "id": "4",
            "isNewUser"：0//是否为新用户
            "nickname": "qqwwe",
            "head_image": "http://192.168.0.88:5656/public/upload/1.jpg",
            "weixinId": "",  //openid，微信用户的唯一标识，也可以用来判断是否绑定微信号
            "signature": "",
            "phone": "",
            "sex": "2",
            "age": "40",
            "session_id": "44c47e0a5eac416073f26e517ab4e717",
            "login_time": "1462342836",
            "register_ip": "127.0.0.1",
            "register_time": "1461911564",
            "imei": "",
            "is_binding": "0",
            "isdel": "0",
            "vip": "0",
            "height": "201",
            "qq": "0",
            "income": "3",
            "marry": "3",
            "province": "",
            "city": "",
            "user_type": "1",
            "ext": {
                "job": "3",
                "education": "3",
                "birthday": "",
                "weight": "",
                "constellation": ""
                "bust": "D"  //罩杯 
            },
            "version_code": "app版本",
            "qq_show": "0",
            "phone_show": "0",
            "online": "1",
            "weixin": "",
            "weixin_show": "0"
            "head_image_status": "0"  // 0:未上传头像 1:头像待审核 2:审核不通过 3:审核通过
            "vip_buy_type": "2"  // 1: vip月卡   2：vip季度卡(季度vip)
            "password": "9876"  // 用户密码(加密前)
        },
      "send_list": {1,2,3}//加上socket之后，向socket请求send接口
    },
    "desc": "登录成功"
}
```