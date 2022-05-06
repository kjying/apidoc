### 查看用户评价

##### HTTP Method: GET
##### URL: https://host/app/index/user_evaluate_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
user_id  |int| 被访问人uid|true|
page|int|页码|true|1
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": [
        {
        uid: "1002974",
        nickname: "莘良俊",
        head_image: "",
        data: [
         {
          content: "完美身材",
          color: "#FC8152"
         },
         {
          content: "成熟稳重",
          color: "#FF66AF"
         },
         {
          content: "火辣",
          color: "#5E8BF1"
         },
        ...
        ]
       },
      ...
     ]
   }
}