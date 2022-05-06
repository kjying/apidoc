### 是否弹出托管提示

##### HTTP Method: GET
##### URL: https://host/app/im/show_auto.php

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
              show: 1,
            }

        ]
    },
    "desc": "查询成功"
}