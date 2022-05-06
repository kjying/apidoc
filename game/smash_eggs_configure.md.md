### 打地鼠配置接口

##### HTTP Method: GET
##### URL: https://host/app/game/smash_eggs_configure.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid  |int| 用户uid|true|
session_id     | string|  |true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 0参数错误 1成功 2未登录 3中奖礼物不存在
        "msg": {
            "goldSmash": 188, // 黄金锤价格
            "thunderSmash": 2188, //雷神之锤价格
            "goldSmashCount": 1, //背包黄金锤数量
            "thunderSmashCount": 0, //背包雷神之锤数量
            "goldGift": [{ // 黄金锤中奖礼物列表
                "type": "3",     // （客户端用不到）
                "gift_id": "1",  // 礼物id
                "num": "88",        // 礼物价格
                "name": "棒棒糖",   // 礼物名称
                "photo_url": "http://leleimg.yewanhuyu.com/gift/2016-09-01_57c7a894b1bad.png",   // 礼物图片
            },
            ...
            ],
            "thunderGift": [{ // 雷神之锤中奖礼物列表
                "type": "4",     // （客户端用不到）
                "gift_id": "4",  // 礼物id
                "num": "1000",        // 礼物价格
                "name": "香蕉",   // 礼物名称
                "photo_url": "http:\/\/leleimg.yewanhuyu.com\/gift\/2016-12-18_585678835a465.png",   // 礼物图片
            }, 
            ...
            ]
        }
    },
    "desc": ""
}