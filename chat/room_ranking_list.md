### 语聊房间榜单

##### HTTP Method: GET
##### URL: https://host/app/chat/room_ranking_list.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
room_id|int|房间id|是|
type|int|类型 1-日榜 2-周榜 3-月榜|是

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": [
            {
                "cost_count": "1617", // 金币数
                "nickname": "呀呼啦啦啦啦啊啊啊", // 用户昵称
                "id": "1001002", // 用户id
                "head_image": "", // 头像
                "sex":"1"
            }
        ]
    },
    "desc": ""
}
```