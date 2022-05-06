### 语聊房间成员是否禁麦

##### HTTP Method: POST
##### URL: https://host/app/chat/room_user_no_speaking.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
room_id|int|房间id|是|
member_id|int|成员id|是
type|int|类型 1-禁言 2-取消禁言|是

##### HTTP Response
```json
{
	'code': 200,
	'data': {
		'result': 1
	},
    'desc': "操作成功"
}
```