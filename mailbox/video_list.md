### 视频列表

##### HTTP Method: Get
##### URL: https://host/app/mailbox/video_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
user_id|int|女主播id|true|测试有一条数据了，user_id=1001317
* socket点赞
数据：'{"event":"video_dianZan","uid":100001,"session_id":"1231","id":1,"type":1}'
注意：id 指视频id，type 1 表示点赞 0 表示取消点赞

已改为http接口：http://git.momohuyu.com/seeklove/seeklove/wikis/mailbox/dian_zan.md

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3
          msg: [ 
            {
                id: "5",//视频id
                anchor_id: "1001317", //女主播id
                url: "http://leleimg.yewanhuyu.com//others_20181011_video_1067120_153927082785078.mp4",
                android_url: "http://leleimg.yewanhuyu.com//others_2018-111_video_1067120_153927082785078.mp4",
                ios_url: "http://leleimg.yewanhuyu.com//others_2018-10-11_video_1067120_153927082785078.mp4",
                is_paycall: "0",
                ctime: "1539309950",
                first_photo: "http://leleimg.yewanhuyu.com//others_2018-10-11_video_1067120_153927082785078.mp4?vframe/png/offset/0",//第一帧图片
                click: 0,//点击数
                is_click: 0, //当前用户是否点赞
                status:0,//0未审核 1 审核
                is_recommend:0,//是否私密视频 0否 1是
                is_show:0//是否可以播放 0否 1是
            },
            {
                id: "5",//视频id
                anchor_id: "1001317", //女主播id
                url: "http://leleimg.yewanhuyu.com//others_20181011_video_1067120_153927082785078.mp4",
                android_url: "http://leleimg.yewanhuyu.com//others_2018-111_video_1067120_153927082785078.mp4",
                ios_url: "http://leleimg.yewanhuyu.com//others_2018-10-11_video_1067120_153927082785078.mp4",
                is_paycall: "0",
                ctime: "1539309950",
                first_photo: "http://leleimg.yewanhuyu.com//others_2018-10-11_video_1067120_153927082785078.mp4?vframe/png/offset/0",//第一帧图片
                click: 0,//点击数
                is_click: 0, //当前用户是否点赞
                status:1,//0未审核 1 审核
                is_recommend:1,//是否私密视频 0否 1是
                is_show:1//是否可以播放 0否 1是
            }
        ],
   },
    desc: ""
}
```