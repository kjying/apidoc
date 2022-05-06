### 打地鼠配置接口

##### HTTP Method: GET
##### URL: https://host/app/game/configure.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid  |int| 用户uid|true|
session_id     | string|  |true|
game_id  |int| 游戏id|true| 
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 0参数错误 1成功 2未登录 3游戏不存在 4游戏特殊属性不存在
        "msg": {       //原样输出
            "GameId": "1001", // 游戏id
            "GameName": "怪物猎人", //游戏名称
            "Status": "1", //状态
            "GiftCount": 0, //账户余额
            "tips_url": '', //游戏规则说明地址
            "DiamondExpendList": [{ // 锤子列表
                "Gold": 10,     // （暂不用）
                "Diamond": 10,  // 金币消耗
                "Lv": 1,        // 开放等级(暂不用)
                "UseCount": 3   // 连击次数
            }, {
                "Gold": 100,
                "Diamond": 100,
                "Lv": 1,
                "UseCount": 4
            }, {
                "Gold": 2000,
                "Diamond": 2000,
                "Lv": 5,
                "UseCount": 5
            }],
            "DiamondGophersList": [{ // 地鼠配置列表
                "GophersId": 101, // 地鼠id
                "KillAward": 15,  // 击杀奖励
                "KillRate": [6864, 10000, 10000], // 消灭概率（客户端不需要）
                "ShowRate": [20, 0, 0] // 出没概率（0木锤、1铁锤、2雷锤）
            }, {
                "GophersId": 102,
                "KillAward": 20,
                "KillRate": [5104, 10000, 10000],
                "ShowRate": [15, 0, 0]
            }, 
            ...
            {
                "GophersId": 115,
                "KillAward": 20000,
                "KillRate": [4, 45, 880],
                "ShowRate": [0, 0, 5]
            }]
        }
    },
    "desc": ""
}