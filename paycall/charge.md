### 用户消费

##### HTTP Method: POST
##### URL: https://host/app/paycall/charge.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
user_id          |int| 女主播id |true|
sub_type         |int| 消费类型：私聊私密图片（30）查看微信（36）查看手机（38）查看QQ（40）查看私密图片（42）查看私密视频（44）|true|
money|int| 金币 |true|
extend|string| 说明(若为私聊私密图片，则该值为该图片的消息id；若为查看私密图片，则该值为图片id；若为查看私密视频，则该值为视频id；)|true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3非法请求 4消费类型错误 5 金币数值错误 6 金币不足 7您操作太快，请重新点击 -1操作数据库发送错误
   },
    desc: "操作成功"//上面的错误信息
}
```