### 用户发送发送语音、图片[new]

##### HTTP Method: POST
##### URL: https://host/app/mailbox/send_file_msg.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid           | int ||true|
session_id| string ||true|
user_id     | int| 接收用户id|true|
content_type | int| 2语音消息，3图片消息|true|
file_url        | url|| 七牛云的文件url|是|
audio_time|int |语音时长|true|0
charge_photo|int |是否为收费图片|true|0
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1     //1发送成功，2未登录，3上传失败
        "msg":{
             "gift_count": "400",  //金币余额 result=1时有返回
             "chat_key": "5000",  //邮票余额 result=1时有返回
        }
    },
    "desc": "发送成功"
}
```