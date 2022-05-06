### 领取话费跑马灯列表

##### HTTP Method: GET
##### URL: https://host/app/index/phone_bill.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---

##### HTTP Response
```json
{
    code: 200,
    data: {
        msg: [ 
            "谷梁高翰领取话费10元",
            "谷梁高翰领取话费10元"
        ],
        result: 1   //1已登录，2未登录
    },
    desc: ""
}
```