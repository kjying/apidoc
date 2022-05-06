### 添加赚钱方案

##### HTTP Method: POST
##### URL: https://host/app/earn/add_plan.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
content | string| 消息内容|true|
gid     | int |礼物id|true|
num     | int |礼物数量|true|
photo   | |表单上传，name随意|false|
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