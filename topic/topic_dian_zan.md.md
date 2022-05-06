### 帖子/回帖点赞（取消点赞）

##### HTTP Method: post
##### URL: https://host/app/topic/topic_dian_zan.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
type|int|点赞/取消点赞 |true|  1（1点赞 0取消点赞）
sub_type|int|帖子/回帖 |true|  1（1帖子 2回帖）
id|int|帖子id/回帖id |true| 

##### HTTP Response
```json
{
    "code": 200, //200 获取成功 400 返回错误信息
    "data": {
        "result": 1,//1成功 2请先登录 3回帖不存在 4举报失败
        "msg": "操作成功"
    }
    "desc": "" // 错误信息
}