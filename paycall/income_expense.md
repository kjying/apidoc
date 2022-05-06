### 收支明细

##### HTTP Method: GET
##### URL: https://host/app/paycall/income_expense.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
page|int|页码|false|1

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, //  1：成功， 2：未登录
        "msg":[
            {
                "id":"123", //记录id
                "type": "1",  //1表示收入，2表示支出
                "sub_type": "提现",  // 项目
                "amount": "20", //  变动的金额
                "account"："1200" //变动后的余额
                "ctime": "1512341520"  //时间戳
            }
        ]
    },
    "desc": ""
}
```