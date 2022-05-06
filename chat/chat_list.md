### 消息列表

##### HTTP Method: GET
##### URL: https://host/app/chat/chat_list.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
before_id|int|上一次获取数据的最后一条content_id|否|0
count|int|数量|否|10


##### HTTP Response
```json
{
	'desc': '',
	'data': {
		'result': 1,
        'is_anchor': False,  //自己是不是主播
		'msg': [{
			'target_user': {    //对方信息
				'head_image': 'http://leleimg.yewanhuyu.com/headImg_2019-09-14_images_5525350_1568469135122.jpg',
				'spend_level': '1',
				'earn_level': '1',
				'level': '1',
				'uid': '1000005',
				'nickname': '果景澄',
				'anchor_status': 1,
				'sex': '1'
			},
			'latest_sender': '1000005', //最近一天聊天记录的发送人
			'latest_content_id': '27',  //最近一条聊天记录id
			'latest_content_time': '1571997258'
			'latest_content': { //最近一条聊天记录信息
				'content_type': '1',
				'content': 'test_msg',
				'ctime': '1571997258',
				'from_uid': '1000005',
				'id': '27',
				'to_uid': '1000004'
			},
			'unread': '2',  //未读记录数
        }],
	},
	'code': 200
}
```