### 回帖

##### HTTP Method: get
##### URL: https://host/app/topic/delete.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
ids|string|帖子id组成的字符串（用逗号分隔）或者回帖id |true|      
type|int|1帖子 2回帖 |false| 1

##### HTTP Response
```json
{
    "code": 200, //200 获取成功 400 返回错误信息
    "data": {
        "result": 1,//1成功 2请先登录 3参数错误 4删除失败
    }
    "desc": "删除成功" //错误信息
}