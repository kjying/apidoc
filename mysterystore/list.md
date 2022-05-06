### 活动页

##### HTTP Method: GET
##### URL: https://host/app/mysterystore/list.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数| | |是

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": [
            {
                "id": "1", // 礼物id
                "gift_name":"四叶草", // 礼物名称
                "gift_icon":"", // 图标
                "gift_value":"10000", // 礼物价值
                "gift_number":"1000", // 礼物份数
                "unit_value":"1000", // 单价
                "purchased_number":"100", // 已购份数
                "current_period":"1", // 当前期数
                "current_start_time":"1572941959", // 当场开始时间
                "current_end_time":"1572941959", // 当场结束时间
                "my_purchased_number":"11", // 我的已购份数
                "is_end":"1", // 是否结束
            }
        ]
    },
    "desc": ""
}
```