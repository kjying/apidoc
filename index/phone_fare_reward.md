### 领取话费

##### HTTP Method: post
##### URL: https://host/app/index/phone_fare_reward.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
id|int|视频id|true|
phone|int|手机号码|true|

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3 视频id错误 4 抱歉，该号段暂不支持 5网络繁忙，请重新提交
          msg:"操作成功"
    },
    desc: ""
}