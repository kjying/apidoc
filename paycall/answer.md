### 用户向主播或主播向用户接收视频请求

##### HTTP Method: GET
##### URL: https://host/app/paycall/answer.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
user_id |int|发送方|true|
call_id |int|通话id|true|
is_check_call |int|1 0表示正常接通|true|0

* 免费试用通话：如果该用户是没有充值的情况下，第一次通话都默认为免费试用

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // -1余额不足，0：妹子已下线，1：成功， 2：未登录，3朋友你动作太快了，休息下再来吧
        "msg":{
            "call_id": '1'  //本次通话的id
            "channelKey": 'ssfdgdg' //声网获取channel_key
             ‘gift_divide_rate’:0.6//本次通话主播的提成比例
             ‘free_video_time’:100 // 免费通话时间
             ‘duke_free_time’:100 // 公爵免费通话时间
             "is_concern":1//1关注 0未关注
        }
    },
    "desc": "xxxxx"
}
```