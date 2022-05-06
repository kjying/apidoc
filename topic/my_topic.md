### 我的帖子（回帖）

##### HTTP Method: GET
##### URL: https://host/app/topic/my_topic.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
page|int| 页数 |true| 1
type|int| 1帖子 2回帖 |true| 1

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 1成功  2未登录
        "msg": [ // 帖子（type=1）
            {
                "id": 1, //帖子id
                "uid": "2294391", //发帖人id
                "reply_count": 5, //回帖数量
                "title": "xxxxxxx", //帖子标题
                "content": "xxxxxxx", //帖子内容
                "nickname": "xxxxxxx", //发帖人昵称
                "head_image": "https://api.iofol.cn/public/upload/head_image/2016-04-28/3-1461826216.png", //发帖人头像
                "status": 0, //帖子状态 0未审核 1审核通过 2审核不通过
                "is_show": 0, // 0正常 1删除
                "time": 1461813260, // 发帖时间
                "photo": { // 帖子图片
                    "http://sl.yiyuqipai.com/public/upload/gift/2016-09-01_57c7a894b1bad.png",
                    "http://sl.yiyuqipai.com/public/upload/gift/2016-09-01_57c7a894b1bad.png",
                    "http://sl.yiyuqipai.com/public/upload/gift/2016-09-01_57c7a894b1bad.png",
                    ...
                }
            }
            ...
        ]
        "msg": [// 回帖 (type=2)
            {
                "id": 1, //回帖id
                "t_id": 1, //帖子id
                "uid": 2294391, //回帖人id
                "reply_uid": 2294391, //被回帖人id
                "content": "xxxxx", //回帖内容
                "status": 0, //状态 0正常  1被举报
                "time": 1461813260, //回帖时间
                "nickname": "xxxxxxx", //回帖人昵称
                "head_image": "https://api.iofol.cn/public/upload/head_image/2016-04-28/3-1461826216.png", //回帖人头像
                "title": "xxxxxxx", //帖子标题
                "photo": { // 帖子图片
                    "http://sl.yiyuqipai.com/public/upload/gift/2016-09-01_57c7a894b1bad.png",
                    "http://sl.yiyuqipai.com/public/upload/gift/2016-09-01_57c7a894b1bad.png",
                    "http://sl.yiyuqipai.com/public/upload/gift/2016-09-01_57c7a894b1bad.png",
                    ...
                }
                "topic_content": "xxxxxxx", //帖子内容
                "reply_nickname": "xxxxxxx", //被回帖人昵称
            }
            ...
        ]
      
    },
    "desc": ""
}
```
