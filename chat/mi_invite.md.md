### 邀请上麦

##### HTTP Method: GET
##### URL: https://host/app/chat/mi_invite.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
room_id|int|房间id|是|
mi_seq|int|麦序0-4|是|
invite_uid|int|邀请对象uid|是|


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
* [mi_invite](room.md)   只发给被邀请人
