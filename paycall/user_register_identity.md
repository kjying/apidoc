### 女性用户注册（v2.0）

##### HTTP Method: POST
##### URL: https://host/app/paycall/user_register_identity.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
real_name  | string |真实实名|true|
ID_number  | string |身份证号码|true|
image_url_1 |url| 七牛云的图片url|是|
image_url_2 |url| 七牛云的图片url|是|
image_url_3 |url| 七牛云的图片url|是|
alipay_id|string | 支付宝账号|是|
video_url |url| 七牛云的小视频url|是|
nickname       | string| 昵称 |true|
imei            |string| imei |true|
version_code    |string| app版本 |true|
channel         |string| 渠道号  |true|
phone         |string| 手机号：如果是手机号码登录，请传该参数|false|
weixin         |string| 微信号|false|
qq         |string| QQ号|false|
weixin_id         |string| 微信：如果是微信登录，请传该参数|false|
head_img         |string|微信头像：上传七牛云之后的url  |false|
signature|string|签名验证  |false|v2.0版本必须传
timestamp|int|时间戳|false|v2.0版本必须传
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