### 点赞

##### HTTP Method: POST
##### URL: https://host/app/beauty/praise.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
topic_id    | int       | 动态id    | true |
is_del    | int       | 取消点赞:1    | false |0

##### HTTP Response
```javascript
{
	'code': 200,
	'data': {
		'count_praise': 1	#新的点赞数
	},
	'desc': ''
}
```