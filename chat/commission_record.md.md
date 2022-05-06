### 聊吧佣金记录

##### HTTP Method: GET
##### URL: https://host/app/chat/commission_record.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
page|int|页码|是

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "record_list": [
                {
                    "uid": "1004605", // 用户id
                    "income_type": "1", // 1: 礼物周结; 2:月度奖励
                    "income_type_name":"礼物周结",
                    "income": "100.00",
                    "ctime": "2019/10/30 10:04:21"
                },
                {
                    "uid": "1004605",
                    "income_type": "2",
                    "income_type_name":"月度奖励",
                    "income": "300.00",
                    "ctime": "2019/10/30 10:04:21"
                }
            ],
            "total_revenue": "400" // 总收益
        }
    },
    "desc": ""
}
```