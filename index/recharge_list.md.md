### 充值跑马灯列表

##### HTTP Method: GET
##### URL: https://host/app/index/recharge_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---

##### HTTP Response
```json
{
    code: 200,
    data: {
        msg: [ 
            "谷梁高翰充值30元",
            "谷梁高翰充值30元"
        ],
        result: 1   //1已登录，2未登录
    },
    desc: ""
}
```