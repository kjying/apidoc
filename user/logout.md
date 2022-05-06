### 用户退出接口

##### HTTP Method: POST
##### URL: https://host/app/user/logout.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid| int||true|
session_id      | string ||true|

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 2  //未登录状态
    },
    "desc": "已成功退出"
}
```