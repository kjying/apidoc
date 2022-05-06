### 获取用户余额

##### HTTP Method: GET
##### URL: https://host/app/game/gift_count.php

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
        "result": 1, // 0参数错误 1成功 2未登录
        "gift_count": 1000 //用户余额
    },
    "desc": ""
}