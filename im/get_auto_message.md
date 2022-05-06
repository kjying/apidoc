### 获取女主播的聊天托管发送消息的内容

##### HTTP Method: Post
##### URL: https://host/app/im/get_auto_message.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
client_id|int|接收发id|true|
type|int|类型 0 发送消息 1 回复消息|true|
发送消息时type参数：
 * 25 主播设置聊天托管后，自动向新用户推送消息；
 * 26 主播设置聊天托管后，自动回复用户消息；
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3非法请求 4该用户未通过实名验证 5该用户未开通聊天托管 6自动发消息的间隔未超过30s
        "msg": [
            {
              content: "测试消息",
            }

        ]
    },
    "desc": "查询成功"
}
