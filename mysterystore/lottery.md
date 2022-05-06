### 参与抽奖

##### HTTP Method: POST
##### URL: https://host/app/mysterystore/lottery.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数| | |
uid|int|用户id |是
session_id|string|session_id|是
gift_id|int|礼物id|是
purchase_number|int|购买数量|是
current_period|int|购买的期数|是
version_code|int|版本号|是
channel|string|渠道|是

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1
    },
    "desc": ""
}
```