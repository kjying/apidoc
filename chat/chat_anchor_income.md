### 聊吧房间主播收益

##### HTTP Method: GET
##### URL: https://host/app/chat/chat_anchor_income.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "day_income": "0", // 当日收益
            "week_income": "0", // 当周收益
            "month_income": "2.60", // 当月收益
            "last_month_income": "0", // 上月收益
        }
    },
    "desc": ""
}
```