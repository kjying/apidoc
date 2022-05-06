### 动态视频列表

##### HTTP Method: Get
##### URL: https://host/app/index/dynamic_video_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
page|int|页数|true|1
type|int|类型 1 推荐 2 最新 3 VIP |true|1

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 
          msg: [ 
            {
                id: "5",//视频id
                anchor_id: "1001317", //女主播id
                nickname: "是妹子啊",
                signature: "好喜欢这张八年级啊姐姐就现在看见啊卡卡卡几点结束计算机三级我看看",
                url: "http://leleimg.yewanhuyu.com//others_20181011_video_1067120_153927082785078.mp4",
                first_photo: "http://leleimg.yewanhuyu.com//others_2018-10-11_video_1067120_153927082785078.mp4?vframe/png/offset/0",//第一帧图片
                click: 0,//点击数
                is_click: 0 //当前用户是否点赞
                is_follow: 0 //当前用户是否关注该主播
                is_identity: 0,//
                video_price: 0,//
                audio_price: 0,//
                level: "12",
                is_recommend: 0, //是否私密视频 0否 1是
                is_show: 1 //是否可以播放 0否 1是
            }, 
            {
                id: "5",//视频id
                anchor_id: "1001317", //女主播id
                nickname: "是妹子啊",
                signature: "好喜欢这张八年级啊姐姐就现在看见啊卡卡卡几点结束计算机三级我看看",
                url: "http://leleimg.yewanhuyu.com//others_20181011_video_1067120_153927082785078.mp4",
                first_photo: "http://leleimg.yewanhuyu.com//others_2018-10-11_video_1067120_153927082785078.mp4?vframe/png/offset/0",//第一帧图片
                click: 0,//点击数
                is_click: 0 //当前用户是否点赞
                is_follow: 0 //当前用户是否关注该主播
                is_identity: 1,
                video_price: "200",
                audio_price: "200",
                level: "12",
                level: "12",
                is_recommend: 0, //是否私密视频 0否 1是
                is_show: 1 //是否可以播放 0否 1是
            }
        ],
   },
    desc: ""
}
```