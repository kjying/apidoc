### 主播备注

##### HTTP Method: GET
##### URL: https://host/app/user/remarks_update.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
uid|int| 主播id |true| 100002
session_id     | string|  |true|
content|string| 备注名称 |true| 
user_id|int| 用户id |true| 100002

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 1成功  2未登录 3参数错误 4请先关注用户 5操作失败
        "msg" [ //用户信息，详细请看session
            "id":1000002
            ...
            "remarks_name":"xxxxx"
        ]
    },
    "desc": "操作成功"
}
```
