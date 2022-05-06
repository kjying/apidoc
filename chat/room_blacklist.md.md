### 房间黑名单列表

##### HTTP Method: GET
##### URL: https://host/app/chat/room_blacklist.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是|
session_id|string|用户id|是|
room_id|int|房间id|是|


##### HTTP Response
```json
{
	'desc': '',
	'data': {
		'result': 1,
		'msg': [{
			'uid':'1', // 用户id         
			'nickname': 'nickname', // 昵称
			'head_image': 'http://baidu.com/1.jpg', // 头像
			'status':'1', // -1:封禁; -9:永久封禁
			'unblock_time': '2019-07-07 15:00', // 解封时间,
            'block_nickname': 'nickname', // 封禁人昵称
		}]
	},
	'code': 200
}
```