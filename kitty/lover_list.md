### 用户列表

##### HTTP Method: GET
##### URL: https://host/app/kitty/lover_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
startIndex     | int       | 之前已经获取的数量 分页(拉取更多)时用      | false | 0
count    | int    | 数量       | false | 10

##### HTTP Response
```javascript
{
	'code': 200,
	'data': {
        'result': 1,
        'msg': [userList],    //同user_list接口返回的数据格式一致  每个用户多一个附加信息info字段
    },
	'desc': ''
}
```