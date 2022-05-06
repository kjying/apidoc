### 推广明细

##### HTTP Method: GET
##### URL: https://host/app/paycall/invite_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, //  1：成功， 2：未登录
        "msg":[
            {
                "user_id":"1024156", //用户id
                "nickname": "默默",  
                "head_image": "https://api.iofol.cn/public/upload/head_image/2016-04-28/3-1461826216.png",  //用户头像
                "total_amount"："480" //可分成
                "total_extend": "4800"  //充值金额
            }
        ],
        "total":480
    },
    "desc": ""
}
```