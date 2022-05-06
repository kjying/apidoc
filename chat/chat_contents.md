### 聊天记录列表

##### HTTP Method: GET
##### URL: https://host/app/chat/chat_contents.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
target_uid|int|对方uid|是|
before_id|int|上一次获取数据的最后一条content_id|否|0
count|int|数量|否|10


##### HTTP Response
```json
{
	'code': 200,
	'desc': '',
	'data': {
		'msg': [{
			'ctime': '1571998143',
			'content_type': '1',
			'id': '28',
			'content': 'test_msg',
			'to_uid': '1000004',
			'from_uid': '1000005'
		}, {
			'ctime': '1571997258',
			'content_type': '1',
			'id': '27',
			'content': 'test_msg',
			'to_uid': '1000004',
			'from_uid': '1000005'
		}],
		'total_unread': 1,
		'result': 1
	}
}
```