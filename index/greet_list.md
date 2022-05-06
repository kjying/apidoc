### 一键打招呼

##### HTTP Method: GET
##### URL: https://host/app/index/greet_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---

##### HTTP Response
```json
{
    code: 200,
    data: {
        msg: [ //字段说明请看session接口
            {
                id: "5",
                nickname: "测试",
                head_image: "",
                sex: "1",
                age: "18",
                vip: "0",
                province: "",
                city: "",
                online: "1",// 1 在线 0下线 2 通话中
            },
            {
                id: "5",
                nickname: "测试",
                head_image: "",
                sex: "1",
                age: "18",
                vip: "0",
                province: "",
                city: "",
                online: "1"

            }
        ],
        result: 1   //1已登录，2未登录 //0 男版每天第二次请求返回的结果
        message:'嗨，你好' //消息
    },
    desc: ""
}
```