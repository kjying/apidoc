### 用户守护主播

##### HTTP Method: GET
##### URL: https://host/app/user/user_guard.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
uid|int| 用户id |true| 100002
type|int| 0查询 1守护 |true| 0
user_id|int| 主播id |true| 100002
gold|int| 守护值 |true| 

##### HTTP Response
```json
{
    "code": 200, // 除了result=1时返回200，其他的都是400
    "data": {
        "result": 1, // 1成功  2未登录 3参数错误 4守护值已更新 5守护失败 6用户扣除金币失败 7主播获得金币失败 8生成用户支出流水失败 9主播不存在 10生成用户收入流水失败
        "gold": 10000 // 当type=1时返回（只返回result和gold，没有msg）
    },
    "desc": "守护成功"
}
```
