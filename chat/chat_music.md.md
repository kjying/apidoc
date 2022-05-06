### 语聊添加歌曲

##### HTTP Method: POST
##### URL: https://host/app/chat/chat_music.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
room_id|int|房间id|是|
music_id|int|歌曲id|是


##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1
     },
    "desc": ""
}
```