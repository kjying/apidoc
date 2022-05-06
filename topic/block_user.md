### 屏蔽用户(的贴子)

##### HTTP Method: get
##### URL: https://host/app/topic/block_user.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
block_uid|int|用户uid|true|      

##### HTTP Response
```json
{
    "code": 200, //200 成功 400 返回错误信息
    "data": {
        "result": 1,
    }
}