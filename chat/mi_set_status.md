### 设置麦位状态

##### HTTP Method: GET
##### URL: https://host/app/chat/mi_set_status.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
room_id|int|房间id|是|
mi_seq|int|麦序0-4|是|
status|int|0:关闭;1:正常|否|不改变
voice_status|int|0:禁麦;1:正常|否|不改变


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
* [mi_status](room.md)
