### 语聊房间设置

##### HTTP Method: POST
##### URL: https://host/app/chat/room_update.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
room_id|int|房间id|是|
img_face|string|头像|否|
name|string|名称|否|
notice|string|公告（最多可输入200个字符）|否|
theme|string|主题(这里传的是主题名称)|否|
label|string|标签|否|

##### HTTP Response
```json
{
	'code': 200,
	'data': {
		'result': 1
	},
    'desc': ""
}
```