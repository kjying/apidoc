### 删除用户

##### HTTP Method: POST
##### URL: https://host/app/user/delUser.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 1成功  2未登录 3操作失败
    },
    "desc": ""
}
```
