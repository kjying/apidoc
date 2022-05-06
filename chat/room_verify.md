### 提交主播认证

##### HTTP Method: POST
##### URL: https://host/app/chat/room_verify.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
real_name|string|姓名|是|
id_number|string|身份证号码|是|
image_url_1|string|身份证正面|是|
image_url_2|string|手持身份证|是|
image_url_3|string|身份证反面|是|
video_url|string|视频url|是|
bank_name| string| 银行名称 |是|
bank_num|string|银行卡账号|是|
bank_province|string|开户省/市|是|
bank_city|string|开户地区|是|
pic1_url|string|图片url|否|
pic2_url|string|图片url|否|
pic3_url|string|图片url|否|
pic4_url|string|图片url|否|
pic5_url|string|图片url|否|
pic6_url|string|图片url|否|


##### HTTP Response
```json
{
	'data': {
		'uid': 1000005
	},
	'code': 200,
	'desc': '已提交审核'
}
```