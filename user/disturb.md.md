### 勿扰模式

##### HTTP Method: post
##### URL: https://host/app/user/disturb.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
type|int|1 开启 0 取消|true|

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3 参数错误 4 操作失败 5 朋友你动作太快了，休息下再来吧（5秒一次）
          msg:"操作成功"
    },
    desc: ""
}
