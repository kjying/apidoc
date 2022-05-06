### 国家配置接口

##### HTTP Method: GET
##### URL: https://host/app/user/country.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 1成功 2国家配置数据不存在
        "msg": [{ // 国家配置列表
                "id": "1",     //
                "name": "China",  // 国家名称（英文）
                "country_name": "中国",        // 国家名称（中文）
                "abbreviation": "CN",   // 国家缩写
                "num": "86",        // 国家编码
                "photo_url": "http://leleimg.yewanhuyu.com/photos/2019-08-12_1565593775.png",   // 国家图标
                "ctime": "1565593777",        // 创建时间
            },
            ...
            ]
    },
    "desc": ""
}