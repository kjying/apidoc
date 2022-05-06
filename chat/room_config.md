### 语聊房间获取标签列表和主题列表

##### HTTP Method: GET
##### URL: https://host/app/chat/room_config.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|


##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "label_list": [ // 标签列表
                {
                    "id": 1, // 标签id
                    "name": "虚拟男友" // 标签名
                }
            ],
            "theme_list": [ // 主题列表
                {
                    "id": 8, // 主题id
                    "theme_name": "女孩", // 主题名称
                    "is_pay": 1, // 是否付费 0-否 1-是
                    "price": 999, // 价格
                    "type": 1, // 类型 1-7天
                    "url": "http://leleimg.yewanhuyu.com/drainage/drainage.jpg", // 主题地址
                    "thumb_url": "http://leleimg.yewanhuyu.com/drainage/drainage.jpg", // 缩略图地址
                }
            ],
            "face_list": [
                {
                    "id": 1, // 表情id
                    "face_url": "http://leleimg.yewanhuyu.com/voicechat/face/1-开心.png", // 表情url
                }
            ],
            "bank_code": {
                "中国建设银行": 105,
                "中国农业银行": 103
            },
            "config_chat_open":1, // 聊吧开关 0-关 1-开
            "config_chat_notice":"1", // 聊吧全服公告开关 0-关 1-开
            "mi_fee": 500, // 上麦金币数
            "danmu_fee": 0, // 发送弹幕金币数
        }
    },
    "desc": ""
}
```