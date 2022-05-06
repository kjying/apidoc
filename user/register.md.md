### 用户快速注册接口

##### HTTP Method: POST
##### URL: https://host/app/user/register.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
nickname       | string| 昵称 |true|
birthday |string| 生日|true|1991-01-01
sex             |int| 性别 1，男  2，女|true|
imei            |string| imei |true|
version_code    |string| app版本 |true|
channel         |string| 渠道号  |true|
phone         |string| 手机号：如果是手机号码登录，请传该参数|false|
token         |string| 如果是微信、Facebook或Google登录，请传该参数|false|
head_img         |string|微信头像：上传七牛云之后的url  |false|
signature|string|签名验证  |false|v2.0版本必须传
timestamp|int|时间戳|false|v2.0版本必须传
inviteUid |int|推广用户id|false|推广必须传
type |int|注册类型|false|3微信 4Facebook 5Google
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, //注册成功 已登录状态
        "msg": {
            "id": 4,  //用户id
            "password": 7099,  //明文密码
            "session_id": "c5c9d7774da06a264a4a130b4bb0454b"
        }，
        "send_list": {1,2,3}//加上socket之后，向socket请求send接口
    },
    "desc": "注册成功"
}
```