### 检查用户是否购买过该主播的微信号/手机号/QQ/图片/视频

##### HTTP Method: get
##### URL: https://host/app/index/user_check_weixin.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
user_id|int|主播id|true|
type|int|查看类型 ：0 微信 1 手机 2 QQ 3 图片 4 视频|true|
extend|int|说明（如果是图片，则该值为图片id；如果是视频，则该值为视频id）|true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1可以查看，2未登录 3 不可以查看(未购买)
        "msg":{
            "weixin":"",
            "phone":"",
            "qq":""
        }
    },
    desc: ""
}
