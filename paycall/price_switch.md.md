### 主播设置自己的语音和视频价格

##### HTTP Method: GET
##### URL: https://host/app/paycall/price_switch.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
video_price|int|视频|是|
audio_price|int|语音|是|


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