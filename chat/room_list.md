### 房间列表

##### HTTP Method: GET
##### URL: https://host/app/chat/room_list.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
room_id|int|搜索id|否|
page|int||否|1
count|int|数量|否|10


##### HTTP Response
```json
{
	'desc': '',
	'data': {
		'my_info': {
			'spend_level': '1',
			'online_level': '1',
			'online_time': '0',
			'uid': '1000005',
			'earn_level': '1',
			'earn': '0',
			'anchor_status': '2',	//0:普通;1:主播;2:主播审核中
			'spend': '0',
			'is_broker': '0'		//0:普通;1:经纪人
		},
		'result': 1,
		'msg': [{
			'name': '果景澄',       //房间名称
			'room_id': '1000005',   //房间id
			'img_face': 'http://leleimg.yewanhuyu.com/headImg_2019-09-14_images_5525350_1568469135122.jpg', //房间封面图
			'level': '1',           //等级
			'count_user': '0',      //用户数
			'notice': '',           //公告
			'label': '其他',        //标签
			'theme': '沙漠',        //主题
			'istop': '0',           //是否置顶
			'uid': '1',           //房主uid
		}]
	},
	'code': 200
}
```