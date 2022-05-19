### 礼物列表

##### HTTP Method: GET
##### URL: https://host/app/paycall/gifts.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||true|

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "normal": [
                {
                    "effect_url": "http://wangsu.huataclub.com/gift/2021-09-06_1630907543.svga",
                    "id": "26",
                    "img": "http://wangsu.huataclub.com/gift/2021-09-06_1630907492.png",
                    "name": "Your name is on my body",
                    "position": "0",
                    "price": "4999",
                    "special": "0"
                },
            ],
            "special": [
                {
                    "effect_url": "http://wangsu.huataclub.com/gift/2021-09-06_1630907543.svga",
                    "id": "26",
                    "img": "http://wangsu.huataclub.com/gift/2021-09-06_1630907492.png",
                    "name": "Your name is on my body",
                    "position": "0",
                    "price": "4999",
                    "special": "1"
                },
            ],
            "show": [
                {
                    "effect_url": "http://wangsu.huataclub.com/gift/2021-09-06_1630907543.svga",
                    "id": "26",
                    "img": "http://wangsu.huataclub.com/gift/2021-09-06_1630907492.png",
                    "name": "Your name is on my body",
                    "position": "0",
                    "price": "4999",
                    "special": "2"
                },
            ],
         }
     }
}