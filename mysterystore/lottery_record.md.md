### 参与纪录

##### HTTP Method: GET
##### URL: https://host/app/mysterystore/lottery_record.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数| | |是
page|int|page|否

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": [
            {
                "period_number":"期数",
                "gift_name":"四叶草",
                "record_code":[
                    "1111",
                    "2222",
                    "3333"
                ], // 参与的码
                "win_code":"1111", // 中奖码 抽中才有值, 否则为 null
                "is_return": 1 // 是否退还, 1-已经退还 0-没有
            }
        ]
    },
    "desc": ""
}
```