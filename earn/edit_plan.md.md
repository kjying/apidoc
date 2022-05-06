### 修改赚钱方案

##### HTTP Method: POST
##### URL: https://host/app/earn/edit_plan.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
pid     | int |方案id|true|
content | string| 消息内容|true|
gid     | int |礼物id|true|
num     | int |礼物数量|true|
photo   | |表单上传，name随意|true|
photo_uri | string |旧相片，将url传上来，多个用,分割（不用传）|false|
image_url       | url| 七牛云的图片url|是|

image_url：多张图片，请用英文‘|’隔开

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