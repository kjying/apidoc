### 语聊房间管理员设置与取消

##### HTTP Method: POST
##### URL: https://host/app/chat/room_admin_setting.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是
session_id|string|session_id|是
room_id|int|房间id|是|
member_id|int|成员id|是
type|int|类型 1-设置为管理员 2-取消管理员身份|是

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