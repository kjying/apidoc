### 查询用户绑定状态

##### HTTP Method: Get
##### URL: https://host/app/user/check_binding.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录
        "msg": [
            {
              “phone”：13112192316，
              “phone_binding”：1,//0未绑定 1绑定
              “weixinId”：""，
              “weixinId_binding”：0,//0未绑定 1绑定

            }

        ]
    },
    "desc": "查询成功"
}

```