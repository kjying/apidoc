### 签到

##### HTTP Method: post
##### URL: https://host/app/index/sign_in.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
id|int|签到id|true|

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3 签到id错误 4 签到已完成，请领取奖励 5您今天已经签到了
          msg:"操作成功"
    },
    desc: ""
}