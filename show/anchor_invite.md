### 主播邀请用户

##### HTTP Method: GET
##### URL: https://host/app/show/anchor_invite.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||true|
user_id|int| 对方用户id|true|
gid|int| 表演礼物id|true|
call_id|int| 通话id|true|


##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "show_id": 1,   //表演id
         }
     }
}