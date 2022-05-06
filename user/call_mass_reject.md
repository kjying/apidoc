### 用户拒接群拨时触发，修改用户群拨状态

##### HTTP Method: get
##### URL: https://host/app/user/call_mass_reject.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
type|int|1视频  2音频| false| 女性必须传  
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 
          msg:"操作成功"
    },
    desc: ""
}