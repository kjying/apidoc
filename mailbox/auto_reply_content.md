### 女主播设置托管后，上线之后群发消息

##### HTTP Method: Get
##### URL: https://host/app/mailbox/auto_reply_content.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3非法请求 4该用户未通过实名验证 5未开启托管功能
        "timer": 60//时间间隔 单位秒
          msg: [ 
            {
                id: "5",
                nickname: "测试",
                head_image: "",
                sex: "1",
                age: "18",
                vip: "0",
                province: "",
                city: "",
                online: "1",
                message：‘小哥哥’，//消息内容
                time：1354542165 //时间戳
                content_type:1,//1文本消息，2语音消息，3图片消息
                audio_time:0//语音时长
            },
            {
                id: "5",
                nickname: "测试",
                head_image: "",
                sex: "1",
                age: "18",
                vip: "0",
                province: "",
                city: "",
                online: "1"，http://leleimg.yewanhuyu.com/chat_2018-09-06_audio_1001307_1536226296975.amr
                message：‘’，//消息内容
                time：1354542165 //时间戳
                content_type:2，
                audio_time:10//语音时长
            }
        ],
   },
    desc: ""
}
```