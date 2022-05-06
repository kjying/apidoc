### 语聊用户发送表情

##### HTTP Method: POST
##### URL: https://host/app/chat/chat_face.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
room_id|int|房间id|是|
face_url|string|表情url|是


##### HTTP Response
```json
{
    'code': 200,
    'data': {
        'result': 1
     },
    "desc": ""
}
```