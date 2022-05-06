### 房间送礼

##### HTTP Method: POST
##### URL: https://host/app/chat/room_gift.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
room_id|int|房间id|是|
gift_id|id|礼物id|是|
count|int|数量|是|
repeat|int|连送计数|否|1
to_uid|int|对象uid|否|
to_uidstring|string|多个对象uid用,分隔|否|

##### HTTP Response
```json
{
	'code': 200,
	'data': {
		'msg': [{
			'room_id': '1000005',
			'get_uid': '1000005',
			'repeat': '1',
			'count': '1',
			'ctime': 1570606174,
			'from': 2,
			'profit': 10,
			'channel': 'test001',
			'send_uid': '1000004',
			'cost': 21,
			'gift_id': '1',
			'version_code': 1
		}, {
			'room_id': '1000005',
			'get_uid': '1000004',
			'repeat': '1',
			'count': '1',
			'ctime': 1570606174,
			'from': 2,
			'profit': 10,
			'channel': 'test001',
			'send_uid': '1000004',
			'cost': 21,
			'gift_id': '1',
			'version_code': 1
		}],
		'result': 1,
		'remain_gift_count': 1,
	},
	'desc': ''
}
```

##### Notify
* [user_gift](room.md)
