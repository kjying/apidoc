### 获取好友列表、关注列表、关注房间列表、粉丝列表

##### HTTP Method: GET
##### URL: https://host/app/chat/chat_follow_list.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
type|int|类型 1-关注房间列表 2-关注人列表 3-好友列表 4-粉丝列表|是
page|int|页码|是

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "room_follow_list": [ // 当请求某种类型列表时, 另外的类型值为空 null
                {
                    "room_id": "1001312", // 房间id
                    "name": "测试用", // 房间名称
                    "label": "其他", // 标签
                    "img_face": "05_.jpg__153075875538835.jpg", // 房间图片
                }
            ],
            "chat_follow_list": [
                {
                    "follow_id": "1001312", // 用户id
                    "nickname": "测试用", // 昵称
                    "head_image": "http://p8x3j9qoc.bkt.clouddn.com/headImg_2018-07-05_.jpg__153075875538835.jpg", // 图片
                    "sex": "1", // 性别
                }
            ],
            "chat_friend_list": [
                {
                    "friend_id": "1001312",
                    "nickname": "测试用",
                    "head_image": "http://p8x3j9qoc.bkt.clouddn.com/headImg_2018-07-05_.jpg__153075875538835.jpg",
                    "sex": "1", // 性别
                }
            ],
            "chat_fans_list": [
                {
                    "uid": "1001312",
                    "nickname": "测试用",
                    "head_image": "http://p8x3j9qoc.bkt.clouddn.com/headImg_2018-07-05_.jpg__153075875538835.jpg",
                    "sex": "1", // 性别
                }
            ],
        }
    },
    "desc": ""
}
```