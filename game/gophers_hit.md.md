### 打地鼠接口

##### HTTP Method: GET
##### URL: https://host/app/game/gophers_hit.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid  |int| 用户uid|true|
session_id     | string|  |true|
game_id  |int| 游戏id|true| 
ToolIndex  |int| 锤子档(索引1开始)|true| 
GophersId  |int| 地鼠Id|true| 
HoleId  |int| 地鼠洞Id|true| 
room_id  |int| 房间号|true| 
version_code  |int| 版本号|true| 
channel  |int| 渠道号|true| 
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 0参数错误 1成功 2未登录 3游戏不存在 4游戏特殊属性不存在 5游戏未开启 6余额不足 7用户扣除金币失败 8生成用户支出流水失败 9增加胜利金币失败 10生成用户收入流水失败 11插入游戏记录失败
        "msg": {       //原样输出
            "HitRes": 1, // 打地鼠结果(1:失败,2:胜利)
            "HitEffect": 0, //打击效果(0:无,1击晕,2:破防,3:雷击)
            "FreeCode": 0, //免费打击码(HitEffect=3时)
            "BufCount": 0, //打击Buf次数(HitEffect>2时)
            "EffectEndTime": 0, //特效结束时间(HitEffect>2时)
            "ToolIndex": 0, //锤子档(索引1开始)
            "GophersId": 0, //地鼠Id
            "HoleId": 0, //地鼠洞Id
            "KillGophers": 0, //打地鼠消耗金币数
            "AfterDiamond": 0, //扣除金币后余额
            "WinDiamond": 0, //消灭地鼠获得金币数
            "AfterWinDiamond": 0, //消灭地鼠后余额
            "gift_count": 0, //余额
        }
    },
    "desc": ""
}