### 下麦

##### HTTP Method: GET
##### URL: https://host/app/chat/mi_leave.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
room_id|int|房间id|是|
target_uid|int|麦上用户uid|否|自己下麦

##### HTTP Response
```json
{
	'code': 200,
	'data': {
		'result': 1,
		'msg': {
		}
	},
	'desc': ''
}
```

##### Notify
* [mi_leave](room.md)
