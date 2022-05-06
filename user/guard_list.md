### 守护列表

##### HTTP Method: GET
##### URL: https://host/app/user/guard_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
uid|int| 用户id |true| 100002
type|int| 0查询自己的守护列表 1用户查询主播守护列表 |true| 0
user_id|int| 主播id 当type=1时传 |true| 100002
page|int| 页数 |true| 1

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 1成功  2未登录 3参数错误
        "msg": [
            {
                "id": 1,
                "uid": "2294391", //守护人（用户）id
                "user_id": '1000002', //主播id
                "gold": "10000", // 守护值
                "free_time": "0",
                "status": 0, //状态 0守护过 1守护中
                "ctime": 1461813260,
                "user_info": { // 守护人信息（用户）
                    "id": "2294391",
                    "nickname": "xxxxxxx", //昵称
                    "head_image": "https://api.iofol.cn/public/upload/head_image/2016-04-28/3-1461826216.png", //头像
                    "level": "1" // 等级
                },
                "anchor_info": { // 被守护人信息（主播）
                    "id": "1000002",
                    "nickname": "xxxxxxx", //昵称
                    "head_image": "https://api.iofol.cn/public/upload/head_image/2016-04-28/3-1461826216.png", //头像
                    "level": "1" // 等级
                }
            },
            ...
        ]
      
    },
    "desc": ""
}
```
