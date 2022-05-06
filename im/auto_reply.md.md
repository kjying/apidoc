### 查询、更改女主播的聊天托管信息

##### HTTP Method: Post
##### URL: https://host/app/im/auto_reply.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
action|string|动作 select or update|true|select
auto_reply_status|int|状态 0 关闭 1 开启|true|0
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3非法请求 4该用户未通过实名验证
        "msg": [
            {
              uid: "18",
              accept_video: "1",
              accept_audio: "1",
              call_video_time: "1524298070",
              call_audio_time: "1524298393",
              greet_time: "0",
              video_price: "300",
              audio_price: "100",
              greet_price: "0",
              ctime: "1523866147",
              rate: "0.40",
              alipay_id: "123456",
              status: "0",
              real_name: "干雪卉",
              guild_num: "cs10022",
              bind_guild_time: "0",
              star_rank: "2",
              auto_reply_status: "0",  //0 关闭 1开启
              nickname: "妫建安",
              head_image: "http://seeklove.momohuyu.com/public/upload/head_image/2018-04-16/18-1523866396.jpg?v=2",
              sex: "2",
              head_image_status: "3",
              gift_count: "16027",
              integral: "6028",
              level: "2"
            }

        ]
    },
    "desc": "查询成功"
}
