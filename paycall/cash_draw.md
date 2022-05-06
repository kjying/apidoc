### 提现

##### HTTP Method: POST
##### URL: https://host/app/pay_call/cash_draw.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|int||true|
amount|int|提现金币数|是|

* amount金币与人民币比例100:1   amount对应的人民币50元起提 且必须50, 60整10


##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "anchorInfo": {
        },
    },
    "desc": "提现成功"
}
```