### 语聊房间成员踢出房间与解封

##### HTTP Method: POST
##### URL: https://host/app/chat/room_user_block.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
room_id|int|房间id|是|
member_id|int|成员id|是
type|int|类型 1-踢出房间 2-解封|是
block_type|int|踢出房间类型 1-5分钟 2-24小时 3-30天 4-永久踢出|否 当type=1时必传

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1
    },
    "desc": "操作成功"
}
```