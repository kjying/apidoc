### 离开房间

##### HTTP Method: GET
##### URL: https://host/app/chat/room_leave.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
room_id|int|房间id|是|


##### HTTP Response
```json
{
	'code': 200,
	'data': {
		'result': 1
	},
	'desc': '已成功退出房间'
}
```

##### Notify
* [room_leave](room.md)