### 关注(取消)房间操作, 关注(取消)主播

##### HTTP Method: POST
##### URL: https://host/app/chat/chat_follow.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
object_id|int|对象id 根据type传对应的值, (1,2 传房间id; 3,4 传对应的用户id)|是
type|int|类型 1-关注房间 2-取消关注房间 3-用户关注主播或者主播关注用户 4-用户取消关注主播或者主播取消关注用户|是

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