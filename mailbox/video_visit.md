### 统计视频观看人数

##### HTTP Method: get
##### URL: https://host/app/mailbox/video_visit.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3 操作失败
          msg:"操作成功"
    },
    desc: ""
}