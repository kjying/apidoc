### 举报回帖

##### HTTP Method: post
##### URL: https://host/app/topic/report.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
reply_id|int|回帖id |true|  

##### HTTP Response
```json
{
    "code": 200, //200 获取成功 400 返回错误信息
    "data": {
        "result": 1,//1成功 2请先登录 3回帖不存在 4举报失败
    }
    "desc": "举报成功" // 错误信息
}