### 投诉举报

##### HTTP Method: POST
##### URL: https://host/app/chat/report.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
user_id|int|对方用户uid|是|
room_id|int|房间id,如果是在房间内举报|否|
content|string|内容|是|
image_url|string|截屏图片url|否|
extend|string|扩展内容 json字符串|否|


##### HTTP Response
```json
{
	'code': 200,
	'data': {
		'result': 1
	},
	'desc': '您的举报已成功提交'
}
```