### 语聊房间设置公告

##### HTTP Method: POST
##### URL: https://host/app/chat/room_set_notice.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
room_id|int|房间id|是|
notice|string|公告（最多可输入200个字符）|是|


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