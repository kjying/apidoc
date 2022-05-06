### 关注与取消关注接口

##### HTTP Method: GET
##### URL: https://host/app/user/follow.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
user_id  |int| 被访问人uid|true|
action   |string| concern:关注 cancel:取消关注 |true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1
    },
    "desc": "关注成功"  //'取消关注成功'
}
```