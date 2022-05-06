### 手机发送验证码接口(暂时用95秀那个第三方接口)

##### HTTP Method: POST
##### URL: https://host/app/user/send_sms.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
type|int|1 视频2语音|true|
phone_country|string|手机国家区号|false|
phone          |  string  |手机号|true|
type           |  int     |验证类型  1表示绑定手机号码 2表示手机号码登录 3表示绑定银行信息|true| 2
app_name       |  string  |应用名|false|乐乐

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1 //1表示发送成功  2表示未登陆
    },
    "desc": "发送成功......"
}
```