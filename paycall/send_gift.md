### 用户送礼

##### HTTP Method: get
##### URL: https://host/app/paycall/send_gift.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
user_id | int | 收礼人id|true|
gid     | int |礼物id|true|
num     | int |礼物数量|true|
call_id| int | 通话id，如果是通话过程中送礼，则必传|false|
pid| int | 主播礼物方案id，安卓>=76,IOS>=52需传|false|
is_backpack| int | 是否为背包送礼|false|


##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, //  1：成功， 2：未登录  3: 余额不足无法送礼
        "msg":{
            "gid"：123  //礼物id
            "gift_count": 40000 //金币余额
        }
    },
    "desc": "送礼成功"
}
```