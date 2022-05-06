### 语聊房间用户信息

##### HTTP Method: GET
##### URL: https://host/app/chat/room_user_info.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
room_id|int|房间id|是
object_id|int|用户id|是

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "uid": "1001002",
            "room_status": "1",  // 用户状态 0:普通; 1:管理员; 2:房主; -1:封禁; -9:永久封禁
            "mi_seq": "-1",// 上麦麦位 0-10; -1表示用户是下麦中
            "in_room": "1",// 是否禁麦 1-正常 0-禁麦
            "mi_status": "1", // 是否禁麦 1-正常 0-禁麦
            "is_follow": true,
            "is_be_follow": false, // 是否被关注
            "is_friend": false,
            "nickname": "呀呼啦啦啦啦啊啊啊",
            "head_image": "",
            "sex": "1",
            "anchor_status": 0, // 是否是主播 0-普通 1-主播 2-待审核
            "level": "1",
            "earn_level": "1", //  魅力等级
            "spend_level": "1" //  财富等级
        }
    },
    "desc": ""
}
```