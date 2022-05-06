### 房间聊天

##### HTTP Method: POST
##### URL: https://host/app/chat/room_chat.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
room_id|int|房间id|是|
content|string|内容|是|
content_type|int|1:文本;2:图片|是|
danmu|int|0:普通;1:弹幕|否|0

##### HTTP Response
```json
{
	'code': 200,
	'data': {
		'msg': {
			'ctime': 1569727771,
			'room_id': '1000005',
			'id': '1',
			'uid': 1000005,
			'content': 'test_msg',
			'content_type': '1',
			'danmu': 0, 		//是否弹幕
		},
		'result': 1
	},
	'desc': ''
}
```

##### Notify
* [user_chat](room.md)
