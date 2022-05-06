### 用户或者主播主动挂断通话

##### HTTP Method: GET
##### URL: https://host/app/paycall/hang_up.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
type|int|1视频  2语音|true|
user_id|int|对方id|true|
call_id|int|通话id|true|  
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // -1：挂断（不结算），1：挂断并返回结算， 2：未登录
        "msg":{
            "other_uid": "1"  //对方id
            "other_nickname":"sfldk", //对方昵称
            "other_head_image":"xxxxxxx", //对方头像
            "total_time": "40", //通话时间，单位秒
            "price": "20", //价格，金币/分钟      如果是主播的，要根据汇率转化成人民币显示
            "amount": "60", //本次费用或者收益    如果是主播的，要根据汇率转化成人民币显示
            "account": "2000", //账户金币余额     如果是主播的，要根据汇率转化成人民币显示
            "role": "user", // 'user'表示用户 ，'anchor'表示主播
            "gift_amount": 100 //本场礼物消费或收益，如果是主播的，要根据汇率转化成人民币显示
        }
    },
    "desc": "xxxxx"  //此处不弹toast
}
```