### 用户向主播或主播向用户发起视频请求

##### HTTP Method: GET
##### URL: https://host/app/paycall/refuse.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
user_id |int|接收方|true|
call_id|int|通话唯一标示|true|
overtime|int|是否超时 1是 0否|true|0

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        “content_type”：4 //4：视频通话请求，5：语音通话请求 
    },
    "desc": "xxxxx"
}
```