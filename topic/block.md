### 屏蔽贴子

##### HTTP Method: get
##### URL: https://host/app/topic/block.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
topic_id|int|帖子id|true|      

##### HTTP Response
```json
{
    "code": 200, //200 成功 400 返回错误信息
    "data": {
        "result": 1,
    }
}