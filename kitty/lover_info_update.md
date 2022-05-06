### 用户附加信息更新

##### HTTP Method: POST
##### URL: https://host/app/kitty/lover_info_update.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
user_id    | int    | 用户id       | true |
info    | string    | 附加信息       | true |

##### HTTP Response
```javascript
{
	'code': 200,
	'data': {
        'uid': 1,
        'info': "",
    },
	'desc': ''
}
```