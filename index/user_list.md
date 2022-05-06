### 首页用户列表

##### HTTP Method: GET
##### URL: https://host/app/index/user_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
type|int|1 最新 2同城 3推荐 4关注 5附近|true|1
page|int|页码|false|1

##### HTTP Response
```json
{
    code: 200,
    data: {
        msg: [ //字段说明请看session接口
            {
                list_type: 1//同城时，当值为1是则作为推荐
                id: "5",
                nickname: "测试",
                head_image: "",
                sex: "2",
                age: "18",
                vip: "0",
                province: "",
                city: "",
                audio_greeting_url: ""//女主播特有 语音url
                audio_time: ""//女主播特有 语音时长
                bust:"C" //女性特有 胸罩
                video_price：200  //女主播特有
                audio_price：200  //女主播特有
                level:10
                online: "1",// 1 在线 0下线 2 通话中
                connection_rate: "89" //接通率
                distant:1.1 km//距离 
                accept_video:1//是否接受视频
                accept_audio:1//是否接受语音
                pay_call_ranking:1//最能聊排行 默认为0
                signature:''//个人签名
                star_rank:3//星级 默认为1
                evaluate: "甜美"//标签
                evaluate_color: "#DB52D1"//标签颜色
                video: ""//主播最新免费小视频
                week_star: 0//主播周星活动排行
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
                level:10
                online: "1"

            }
        ],
        result: 1   //1已登录，2未登录
    },
    desc: ""
}
```