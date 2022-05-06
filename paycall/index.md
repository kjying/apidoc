### 视频语音聊天主页面

##### HTTP Method: GET
##### URL: https://host/app/paycall/index.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
page|int|页码|false|1

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 1成功  2未登录
        "total": 0,
        "list":[
            {
                "uid":14545454,
                "head_image":"xxxxxxxx",
                "nickname":"xxxxx",
                "sex":"2",
                "video_price": "10",
                "audio_price": "10",
                "accept_video": "1",
                "accept_audio": "0"
                "status": -1,   //-1离线, 0通话中, 1空闲
            }
            ...更多
        ]
        

    },
    "desc": ""
}
```