### 发起方轮询（6s一次）

##### HTTP Method: GET
##### URL: https://host/app/paycall/launch_alive.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
type|int|1视频  2语音|true|
user_id|int|接收方|true|
call_id|int|通话id|true|  
roger   |int|默认为0，收到第一帧流后轮询，传roger=1|true| 
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // -1：金币不足中断（返回结算），0: 持续接通中， 1：通话常规中断（返回结算）， 2：未登录
        "msg":{
            "other_uid": "1"  //对方id
            "other_nickname":"sfldk", //对方昵称
            "other_head_image":"xxxxxxx", //对方头像
            "total_time": "40", //通话时间，单位秒
            "price": "20", //价格，金币/分钟   如果是主播的，要根据汇率转化成人民币显示
            "amount": "60", //本次费用或者收益 如果是主播的，要根据汇率转化成人民币显示
            "account": "2000", //账户金币余额  如果是主播的，要根据汇率转化成人民币显示
            "role": "user", // 'user'表示用户 ，'anchor'表示主播
            "gift_amount": 100 //本场礼物消费或收益，如果是主播的，要根据汇率转化成人民币显示
        },
        "screenshot_interval": 10 //截屏间隔，单位秒。当该字段不存在或返回0，用本地默认的0，0则不截屏
    },
    "desc": "xxxxx" //注意：result为-1或1（即返回结算页）时，要toast弹出desc。如果desc为''，则不弹
}
```