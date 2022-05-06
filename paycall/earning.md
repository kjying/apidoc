### 赚钱页

##### HTTP Method: GET
##### URL: https://host/app/paycall/earning.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 1：成功， 2：未登录
        "now_time": "125432222", //当前时间戳
        "msg": {
            "again_call_video_time"："",  //视频可以再次点击的时间
            "again_call_audio_time"："",  //语音可以再次点击的时间
            "again_greet_time"："",       //打招呼可以再次点击的时间
            "accept_video"："",           //是否接收视频。 1接收，0不接受
            "accept_audio"："",           //是否接收语音。 1接收，0不接受
            "is_identity"："",            //是否通过认证， 1通过，0没通过
            "call_video_profit"："",      //视频每分钟收益，元
            "call_audio_profit"："",      //语音每分钟收益，元
            "greet_profit"："",           //打招呼收益，元
            "video_price": 300,           //视频金额
            "audio_price": 100,           //语音金额
            "video_limit_lower": 200,     //视频金额设置下限
            "video_limit_upper": 400,     //视频金额设置上限
            "voice_limit_lower": 100,     //语音金额设置下限
            "voice_limit_upper": 200      //语音金额设置上限
            "anchor_task":1               //是否开启今日任务 1开启 0不开启
            "audio_greeting_status": "0", //0未审核;1:审核通过;2:审核拒绝
            "audio_greeting_url": "",     //打招呼音频url
        }
    },
    "desc": "xxxxx"
}
```