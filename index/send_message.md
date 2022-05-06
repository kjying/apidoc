### 微信小程序发送消息

##### HTTP Method: post
##### URL: https://host/app/index/send_message.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
form_id|string| |true|      
open_id|string| |true| 用户openid
anchor_id|string| |true| 主播id
uid|string| |true|   用户id
session_id|string| |true| 
##### HTTP Response
```json
{
    "code": 200, //200 获取成功 400 返回错误信息
    "data": {}
    "desc": "发送成功"
}
``` 