### 主播群发视频或语音通知

##### HTTP Method: GET
##### URL: https://host/app/paycall/call_mass.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
type|int|1视频  2音频| true|  
is_vip|int|0 代表第一次发起请求，1 代表继续发起该请求| true|0


##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, //  0：未通过实名认证， 1：成功， 2：未登录 
        "msg": {
            "price": 0.02   //价格，元
            "receive_num": 15  //发送给15人
        }
        "send_list":{1,2,3}//加上socket之后，向socket请求send接口
    },
    "desc": "xxxxx"
}
```