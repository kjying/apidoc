### 接受邀请上麦

##### HTTP Method: GET
##### URL: https://host/app/chat/mi_invite_accept.php


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

##### Notify
* [mi_occupy](room.md)