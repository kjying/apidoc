### 首页视频列表（小程序）

##### HTTP Method: Get
##### URL: https://host/app/index/video_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
page|int|页数|true|1

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 
         total：12//总页码 每页默认10个
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
                is_click: 0 //当前用户是否点赞
                status:0//0未审核 1 审核
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
                is_click: 0 //当前用户是否点赞
                status:1//0未审核 1 审核
            }
        ],
   },
    desc: ""
}
```