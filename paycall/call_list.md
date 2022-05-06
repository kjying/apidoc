### 通话列表


##### HTTP Method: GET
##### URL: https://host/app/paycall/call_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
page|int|页码|否|1
pagesize|int|数量|否|20


##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "records": [
            {
                "id": 1970,
                "type": 2,    //1:视频; 2:语音
                "duration": 2,  //时长(秒)
                "start_time": 1536858624, //开始时间utc
                "fare": 100,    //男用户花费
                "profit": 0     //女主播收益
                "user_id":1000012 //对方id
                "user_name":'测试用户1000012' //对方id
            },
            {
                "id": 1969,
                "type": 1,
                "duration": 2,
                "start_time": 1536858613,
                "fare": 203,
                "profit": 0
                "user_id":1000012 //对方id
                "user_name":'测试用户1000012' //对方id
            },
            {
                "id": 1968,
                "type": 2,
                "duration": 3,
                "start_time": 1536857843,
                "fare": 100,
                "profit": 0
                "user_id":1000012 //对方id
                "user_name":'测试用户1000012' //对方id
            },
            {
                "id": 1967,
                "type": 1,
                "duration": 2,
                "start_time": 1536857830,
                "fare": 203,
                "profit": 0
                "user_id":1000012 //对方id
                "user_name":'测试用户1000012' //对方id
            },
            {
                "id": 1966,
                "type": 2,
                "duration": 3,
                "start_time": 1536857814,
                "fare": 100,
                "profit": 0
                "user_id":1000012 //对方id
                "user_name":'测试用户1000012' //对方id
            }
        ]
    },
    "desc": ""
}
```