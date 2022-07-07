### 动态详情

##### HTTP Method: GET
##### URL: https://host/app/beauty/topic_detail.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
topic_id    | int    | 动态id       | true |

##### HTTP Response
```javascript
{
	'code': 200,
	'data': topic_info_detail,
	'desc': ''
}
```
[topic_info_detail](entity_topic_info_detail.md)
```javascript
{
	'code': 200,
	'data': {
		'id': 123,
		'title': 'title-1646898758',
		'uid': 1764593,
		'pic_url': 'https://privme.oss-accelerate.aliyuncs.com/spread/down_pics/6.jpg',
		'desc': 'desc-1646898758',
		'count_comment': 1,
		'count_praise': 0,
		'price': 0,
		'myPraise': 0,
		't_create': 1646898758,
		'nickname': 'pink pussy',
		'head_image': 'http://wangsu.huataclub.com/headImg_2022-03-05_images_1764593_1646484629725.jpg',
		'pics': [{
			'id': 334,
			'topic_id': 123,
			'uid': 1764593,
			'url': 'https://privme.oss-accelerate.aliyuncs.com/spread/down_pics/6.jpg',
			't_create': 1646898758
		}, {
			'id': 335,
			'topic_id': 123,
			'uid': 1764593,
			'url': 'https://privme.oss-accelerate.aliyuncs.com/spread/down_pics/5.jpg',
			't_create': 1646898758
		}, {
			'id': 336,
			'topic_id': 123,
			'uid': 1764593,
			'url': 'https://privme.oss-accelerate.aliyuncs.com/spread/down_pics/1.jpg',
			't_create': 1646898758
		}],
		'comments': [{
			'id': 19,
			'topic_id': 123,
			'content': 'comment-1646898758',
			't_create': 1646898759,
			'reported': 0,
			'uid': 1764593,
			'nickname': 'pink pussy',
			'head_image': 'http://wangsu.huataclub.com/headImg_2022-03-05_images_1764593_1646484629725.jpg',
		}]
	},
	'desc': ''
}
```