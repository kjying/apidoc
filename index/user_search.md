### 用户搜索接口

##### HTTP Method: GET
##### URL: https://host/app/index/user_search.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
keyword  |string| 主播ID或者主播昵称|true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "id": "1",
            "nickname": "8585",
            "head_image": "http://192.168.0.88:5656/public/upload/B.png",
            "signature": "我就呵呵", //用户签名
            "age": "40",
            "height": "170",
            "city": "广州市",
            "is_concern": 0,    // 0表示未关注，1表示已关注，2表示隐藏关注图标(自己访问自己)
        }
    },
    "desc": ""
}
```