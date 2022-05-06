### 用户向主播或主播向用户发起视频请求

##### HTTP Method: GET
##### URL: https://host/app/paycall/call.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
type|int|1 视频2语音|true|
user_id |int|接收方|true|
is_call_mass |int|1表示来自群发呼叫，0表示用户普通呼叫|true|0

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
             "free_video":1 //是否免费试用视频
             ‘gift_divide_rate’:0.6
             ‘free_video_time’:100 // 免费通话时间
             ‘duke_free_time’:100 // 公爵免费通话时间
             "is_concern":1//1关注 0未关注
        }
    },
    "desc": "xxxxx"
}
```