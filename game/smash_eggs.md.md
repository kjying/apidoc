### 打地鼠配置接口

##### HTTP Method: GET
##### URL: https://host/app/game/smash_eggs.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid  |int| 用户uid|true|
session_id     | string|  |true|
tool_index     | string| 锤子档(索引1开始 1黄金锤 2雷神之锤) |true|
count     | string| 砸蛋次数 |true|
version_code     | string| 版本号 |true|
channel     | string| 渠道号 |true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 0参数错误 1成功 2未登录 3活动已结束 4中奖礼物不存在 5余额不足 6用户扣除金币失败 7生成用户支出流水失败 8增加胜利金币失败 9生成用户收入流水失败 10插入游戏记录失败
        "msg": {
            "goldSmashCount": 1, //背包黄金锤数量
            "thunderSmashCount": 0, //背包雷神之锤数量
            "win_prizes": [{ // 黄金锤中奖礼物列表
                "id": "20",     // （客户端用不到）
                "type": "4",  // 
                "gift_id": "4",        // 礼物id
                "num": "4",        // 礼物价格
                "name": "棒棒糖",   // 礼物名称
                "photo_url": "http://leleimg.yewanhuyu.com/gift/2016-09-01_57c7a894b1bad.png",   // 礼物图片
            },
            ...
            ]}
        }
    },
    "desc": ""
}