### 小程序获取手机号码

##### HTTP Method: get
##### URL: https://host/app/index/get_phone_number.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
openid|string| |true|      
encryptedData|string| |true|  
iv|string| |true| 
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,// 1获取成功 2参数不能为空 3sessionKey失效 4获取失败 返回errCode
        "data":{
         }
     }
    "desc": "获取成功"
}
``` 