### 一键打招呼发送消息

##### HTTP Method: Get
##### URL: https://host/app/mailbox/say_hello.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid           | int ||true|
session_id| string ||true|
uid_list     | string| 接收用户列表，多个id请用英文逗号隔开|true|
content | string| 消息内容|false|若为空，则随机发送
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1     //1发送成功，2未登录，3被禁言 4 缺少用户列表
        "msg":‘发送成功’，
        "content ":'hello'
    },
    "desc": ""
}
```