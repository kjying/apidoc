### 通话过程中自动截屏上传(主播请求，约10s一次)

##### HTTP Method: POST
##### URL: https://host/app/paycall/user_upload_screen.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid           | int ||true|
session_id| string ||true|
user_id        | int| |true|
call_id        | int| |true|
screenshot| file| 文件上传（弃用）|false|
image_url        | url|| 七牛云的图片url|true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,  // 1成功  2未登录
    },
    "desc": ""
}
```