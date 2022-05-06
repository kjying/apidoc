### 通话播放视频完成

##### HTTP Method: GET
##### URL: https://host/app/paycall/call_video.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
anchorUid    | int       | 主播uid    | true |
url     | string    | 实际播放视频的url      | true |

##### HTTP Response
```javascript
{
	'code': 200,
	'data': {
	},
	'desc': ''
}
```