### 上麦

##### HTTP Method: GET
##### URL: https://host/app/chat/mi_occupy.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
room_id|int|房间id|是|
mi_seq|int|麦序0-4|是|


##### HTTP Response
```json
{
	'code': 200,
	'data': {
		'result': 1,
		'msg': {
			'token': '006a8243640350748fbab25512580cbfb6fIADiXyQztL5NgzGSD2FOIY34J6qLVFmpIsPj01Enj+VekVIhlmvEEZEcIgAvmwAAK42NXQQAAQAAAAAAAwAAAAAAAgAAAAAABAAAAAAA'
		}
	},
	'desc': ''
}
```

* 进入房间时的token是按角色RoleAttendee生成, 上麦时用RolePublisher重新生成token

##### Notify
* [mi_occupy](room.md)
