### 查看用户收礼列表接口

##### HTTP Method: GET
##### URL: https://host/app/index/user_gift_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
user_id  |int| 被访问人uid|true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": [{
         {
          id: "1",
          img: "http://sl.yiyuqipai.com/public/upload/gift/2016-09-01_57c7a894b1bad.png",
          num: 0,
          name:"棒棒糖"
         },
         {
          id: "2",
          img: "http://sl.yiyuqipai.com/public/upload/gift/2016-09-01_57c7a900dfd9c.png",
          num: 1757,
          name:"棒棒糖111111111"
         },
         .
         .
         .      
         }]
     }
}