### 视频列表

##### HTTP Method: post
##### URL: https://host/app/mailbox/video_upload.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
video_url|string|视频链接 mp4|true|
is_public|int|0 普通视频 1发布动态|true|0
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 
          msg:‘’,
   },
    desc: ""
}
```