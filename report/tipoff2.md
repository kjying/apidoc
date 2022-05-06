### 通话中举报

##### HTTP Method: POST
##### URL: https://host/app/report/tipoff2.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid           | int ||true|
session_id| string ||true|
user_id        | int|被举报人id |true|
user_reason | string|举报理由,直接把选中的那两个汉字上传 |true|
extend          | string|补充信息，可为空 |true|
screenshot| file| 文件上传（弃用）|false|
image_url        | url|| 七牛云的图片url(report)|true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,  // 1成功  2未登录
    },
    "desc": "你的举报已成功提交"
}