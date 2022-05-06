### 小程序获取openid

##### HTTP Method: get
##### URL: https://host/app/index/get_openid.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
js_code|string| |true|      
##### HTTP Response
```json
{
    "code": 200, //200 获取成功 400 返回错误信息
    "data": {
        "openid": 'sdfsdfsdfsdfsdfs',
     }
    "desc": "获取成功"
}
``` 