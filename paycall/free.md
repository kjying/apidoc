### 免费试用视频推荐一个女主播

##### HTTP Method: GET
##### URL: https://host/app/paycall/free.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
type         |int| 类型(1免费试用视频 2选聊) |true|

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 1成功  2未登录
        "total": 0,  // 0 没有 1 1个
        "list":
            {
                "uid":14545454,
                "head_image":"xxxxxxxx",
                "nickname":"xxxxx",
                "sex":"2",
                "video_price": "10",
                "audio_price": "10",
                "accept_video": "1",
                "accept_audio": "0"
                "status": 0,   //-1离线, 0通话中, 1空闲
            }
      
    },
    "desc": ""
}
```
