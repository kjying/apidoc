### 发布动态

##### HTTP Method: POST
##### URL: https://host/app/beauty/topic_create.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
pic_urls    | string    | 图片url 多个图片用;分隔     |true |
title       | string    | 标题                      |true |
desc        | string    | 描述                      |false |

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
		'title': 'title-1646900487',
		'uid': 1764593,
		'pic_url': 'https://privme.oss-accelerate.aliyuncs.com/spread/down_pics/3.jpg',
		'desc': 'desc-1646900487',
		'count_comment': 0,
		'count_praise': 0,
		't_create': 1646900488,
		'id': 145,
		'nickname': 'pink pussy',
		'head_image': 'http://wangsu.huataclub.com/headImg_2022-03-05_images_1764593_1646484629725.jpg',
		'pics': [{
			'id': 400,
			'topic_id': 145,
			'uid': 1764593,
			'url': 'https://privme.oss-accelerate.aliyuncs.com/spread/down_pics/3.jpg',
			't_create': 1646900488
		}, {
			'id': 401,
			'topic_id': 145,
			'uid': 1764593,
			'url': 'https://privme.oss-accelerate.aliyuncs.com/spread/down_pics/5.jpg',
			't_create': 1646900488
		}, {
			'id': 402,
			'topic_id': 145,
			'uid': 1764593,
			'url': 'https://privme.oss-accelerate.aliyuncs.com/spread/down_pics/7.jpg',
			't_create': 1646900488
		}],
		'comments': []
	},
	'desc': ''
}
```
