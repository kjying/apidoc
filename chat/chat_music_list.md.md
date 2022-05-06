### 获取曲库

##### HTTP Method: GET
##### URL: https://host/app/chat/chat_music_list.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
room_id|int|房间id|否
type|int|类型0-获取曲库 1-当前房间已点|否

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": [
            {
                "id": 1, // 歌曲id
                "music_name": "Kiss The Rain", // 歌曲名                
                "singer": "name", // 歌手
                "music_url": "http://leleimg.yewanhuyu.com/voicechat/music/Kiss The Rain.mp3", // 歌曲url 
            }
        ]
    },
    "desc": ""
}
```