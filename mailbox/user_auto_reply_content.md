### v2.4 行为托管

##### HTTP Method: Get
##### URL: https://host/app/mailbox/user_auto_reply_content.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
user_id|int|女主播id|true|
num|int|次数 客户端轮训次数|true|
公共参数||||
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3参数错误 4该功能已关闭 5该主播当天已经发过给这个用户行为托管消息 6本次行为托管消息的条数已达到上限 7该主播没有开启托管 8该主播不在线
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