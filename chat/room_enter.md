### 进入房间

##### HTTP Method: GET
##### URL: https://host/app/chat/room_enter.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
room_id|int|房间id|是|


##### HTTP Response
```json
{
	'data': {
		'my_follow': False,
		'msg': {
			'mi_users': [{
				'mi_seq': 0,
				'status': 1,		//1:正常; 0:关闭;
				'voice_status': 1,	//1:正常; 0:禁麦
				'user': {
					'level': '16',
					'head_image': 'http://leleimg.yewanhuyu.com/headImg_2019-09-14_images_5525350_1568469135122.jpg',
					'uid': '1000005',
					'nickname': '果景澄',
					'room_status': 0,	//0:普通; 1:管理员; 2:房主
				},
			}, {
				'mi_seq': 1,
				'status': 1
			}, {
				'mi_seq': 2,
				'status': 1
			}, {
				'mi_seq': 3,
				'status': 1
			}, {
				'mi_seq': 4,
				'status': 1
			}],
			'img_face': 'http://leleimg.yewanhuyu.com/headImg_2019-09-14_images_5525350_1568469135122.jpg',
			'notice': '',
			'theme': 'default',
			'label': '标签',
			'count_user': '6',
			'name': '果景澄',
			'room_id': '1000005',
			'level': '1'
		},
		'result': 1,
		'token': '006a8243640350748fbab25512580cbfb6fIAB9F+zWE/erMlYgJliL4wKPE8945CdbFgALPT7dF85VllIhlmtSIZZrIgCyMQEAt+eNXQQAAQAAAAAAAwAAAAAAAgAAAAAABAAAAAAA',
		'room_status': 2,
		'room_owner': {
			'level': '16',
			'head_image': 'http://leleimg.yewanhuyu.com/headImg_2019-09-14_images_5525350_1568469135122.jpg',
			'uid': '1000005',
			'nickname': '果景澄',
			'room_status': 0,	//0:普通; 1:管理员; 2:房主,
			'sex' : 1,
		},
		'my_info': {
			'room_status': '1',
			'earn_level': '1',
			'online_level': '1',
			'head_image': '',
			'spend_level': '1',
			'level': '1',
			'uid': '1000004',
			'nickname': '徐和志',
			'sex': '1',
			'anchor_status': 0
		},
		"chat_music": {
			"id": "1", // 歌曲id
			"uid": "12345", // 用户id
			"singer": "name", // 歌手
			"music_name": "name", // 歌曲名
			"music_url": "http://leleimg.yewanhuyu.com/voicechat/music/Kiss The Rain.mp3", // 歌曲url
		}
	},
	'desc': '',
	'code': 200
}
```
* 麦位status: 0:关闭, 1:正常, 9:禁坐

* 如果用户被封禁进入房间时: result = 5, desc = '提示信息'

##### Notify
* [room_enter](room.md)
