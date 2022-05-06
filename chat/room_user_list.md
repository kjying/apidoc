### 语聊房间用户列表

##### HTTP Method: GET
##### URL: https://host/app/chat/room_user_list.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
room_id|int|房间id|是|
page|int|页码,只对作用于用户列表,管理员列表是一次性返回所有|是

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "user_count": "7", // 房间人数
            "room_admin_list": [ // 管理员列表, 一次性返回所有管理员
                {
                    "uid": "1001312", // 用户id
                    "room_status": "2", // 用户状态 0:普通; 1:管理员; 2:房主; -1:封禁; -9:永久封禁
                    "mi_seq": "0", // 上麦麦位 0-10; -1表示用户是下麦中
                    "mi_status": "0", // 是否禁麦 1-正常 0-禁麦
                    "nickname": "测试用", // 昵称
                    "head_image": "http://clouddn.com/1.jpg", // 头像
                    "sex": "1", // 性别 1:男 2:女
                    "is_follow": true, // 是否已经关注 true-是 false-否
                    "is_friend": true, // 是否好友 true-是 false-否
                    "anchor_status": '0', // 是否是主播 0-普通 1-主播 2-待审核
                    "spend_level": '0', //  财富等级
                    "earn_level": '0', //  魅力等级
                }
            ],
            "room_user_list": [ // 成员列表,根据页码返回
                {
                    "uid": "1004796", // 用户id
                    "room_status": "0", // 用户状态 0:普通; 1:管理员; 2:房主; -1:封禁; -9:永久封禁
                    "mi_seq": "0", // 上麦麦位 0-10; -1表示用户下麦中
                    "mi_status": "0", // 是否禁麦 1-正常 0-禁麦
                    "in_room": "0", // 是否在线 0:不在线 1:在线
                    "nickname": "别高昂", // 昵称
                    "head_image": "", // 头像
                    "sex": "1" // 性别 1:男 2:女
                    "is_follow": true, // 是否已经关注 true-是 false-否
                    "is_friend": true, // 是否好友 true-是 false-否
                    "anchor_status": '0', // 是否是主播 0-普通 1-主播 2-待审核
                    "spend_level": '0', //  财富等级
                    "earn_level": '0', //  魅力等级
                }
            ]
        }
    },
    "desc": ""
}
```