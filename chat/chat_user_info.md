### 聊吧个人空间

##### HTTP Method: GET
##### URL: https://host/app/chat/chat_user_info.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
object_id|int|对象id|是
room_id|int|房间id,需要查看房间信息是需要|否

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "uid": 1004605,
            "nickname": "亓官高翰",
            "photos": [
                {
                    "path": "http://leleimg.yewanhuyu.com/photos_2019-10-29_images_1004605_1572332332465.jpg", // 图片
                    "thumb": "http://leleimg.yewanhuyu.com/photos_2019-10-29_images_1004605_1572332332465.jpg", // 缩略图
                }
            ],
            "signature": "卡可口可乐了看看", // 签名
            "spend_level": "1", // 财富等级
            "spend": "1", // 财富值
            "earn_level": "1", // 魅力等级
            "earn": "1", // 魅力值
            "count_follow": "1", // 粉丝数
            "height": "170", // 身高
            "weight": "60kg", // 体重
            "age": "23", // 年龄
            "constellation": "摩羯座", // 星座
            "head_image": "http://leleimg.yewanhuyu.com/572332332465.jpg",
            "sex": "1",
            "is_follow": true, // 是否关注
            "is_be_follow": true, // 是否被关注
            "is_friend": false, // 是否好友
            "anchor_status": "0", // 是否主播: 0:普通;1:主播;2:待审核
            "room_status": "0", // 用户状态 0:普通; 1:管理员; 2:房主; -1:封禁; -9:永久封禁
            "mi_seq": "1" // 上麦麦位 0-10; -1表示用户下麦中
        }
    },
    "desc": ""
}
```