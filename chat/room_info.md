### 获取房间信息

##### HTTP Method: GET
##### URL: https://host/app/chat/room_info.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
room_id|int|房间id|是

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "name": "测试用的的",
            "room_id": "1001312",
            "img_face": "05_.jpg__153075875538835.jpg",
            "notice": "广告位招租",
            "theme": "http://leleimg.yewanhuyu.com/drainage/drainage.jpg",
            "label": "其他",
            "name_status": 1, // 状态，1-审核中 2-审核不通过 3-审核通过
            "img_face_status": 3,
            "notice_status": 1
        }
    },
    "desc": ""
}
```