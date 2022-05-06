### 主播设置语音打招呼模板

##### HTTP Method: POST
##### URL: https://host/app/paycall/upload_audio_greeting.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
audio_url|string|语音url|是|
audio_len|string|语音长度|是|10


##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1
    },
    "desc": ""
}
```