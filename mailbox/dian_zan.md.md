### 点赞

##### HTTP Method: post
##### URL: https://host/app/mailbox/dian_zan.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
id|int|视频id|true|
type|int|1 点赞 2 取消点赞|true|

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3 视频id错误 4 操作失败
          msg:"操作成功"
    },
    desc: ""
}
