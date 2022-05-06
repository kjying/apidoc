### 创建房间

##### HTTP Method: POST
##### URL: https://host/app/chat/room_create.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
name|string|名称|否|用户昵称
img_face|string|头像|否|用户头像
label|string|标签|否|其他
theme|string|主题|否|沙漠
notice|string|公告|否|


##### HTTP Response
```json
{
	'desc': '',
	'data': {
		'result': 1,
		'msg': {
			'name': '果景澄',       //房间名称
			'room_id': '1000005',   //房间id
			'img_face': 'http://leleimg.yewanhuyu.com/headImg_2019-09-14_images_5525350_1568469135122.jpg', //房间封面图
			'level': '1',           //等级
			'count_user': '0',      //用户数
			'notice': '',           //公告
			'label': '其他',        //标签
			'theme': '沙漠',        //主题
			'istop': '0',           //是否置顶
		}
	},
	'code': 200
}
```