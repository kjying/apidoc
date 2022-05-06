### 聊天

##### HTTP Method: POST
##### URL: https://host/app/chat/chat_send.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
content|string|内容|是|
content_type|int|1:文本;2:图片|是|
to_uid|int|对方uid|是|

##### HTTP Response
```json
{
	'code': 200,
	'data': {
		'result': 1
	},
	'desc': ''
}
```

##### Notify
```json
{
	"event": "chat_new",    //有新的消息
	"sender_uid": "111",
}
```