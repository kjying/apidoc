### 排行榜

##### HTTP Method: GET
##### URL: https://host/app/index/ranking.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
sub_type|int|1财富榜，2明星榜，3人气榜，4女神榜，5男神榜 6 最能聊 7亲密榜 8守护榜|true|1
user_id|int|主播id 当sub_type=7必须传|false|0

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,  // 1成功，2未登录 3.参数错误(当sub_type=7必须传user_id)
        "list": [
            {
                "list_day": 0, //日榜 0未上榜 1上榜
                "list_week": 0, //周榜 0未上榜 1上榜
                "list_month": 0, //月榜 0未上榜 1上榜
                "list_all": 0, //总榜 0未上榜 1上榜
            }
        ],
        "day_rank": [ //日榜。
            {
                "user_id": "28150903",  //用户id
                "score": "14750", //得分值，可以无视（守护榜时为守护值）
                "nickname": "因子", // 昵称
                "head_image": "", //头像
                "head_image_status": "0", //头像审核状态
                "level": "4", //等级
                "sex": "1", //性别
                "video_price": 0, //视频价格
                "audio_price": 0 //语音价格
                "user_info": {
                    "uid":"1004170"
                    "user_nickname":"巴驰海"
                    "user_head_image":""
                    "user_head_image_status":"1"
                    "user_level":"27"
                    "user_sex":"1"
                }
            },
            ...
        ],
        "week_rank": [ //周榜
            {
                "user_id": "28226279",
                "score": "93200",
                "nickname": "a飞龙飞",
                "head_image": "",
                "head_image_status": "0",
                "level": "5",
                "sex": "1",
                "video_price": 0, //视频价格
                "audio_price": 0 //语音价格
                "user_info": {
                    "uid":"1004170"
                    "user_nickname":"巴驰海"
                    "user_head_image":""
                    "user_head_image_status":"1"
                    "user_level":"27"
                    "user_sex":"1"
                }
            },
            ...
        ],
        "month_rank": [ //月榜
            {
                "user_id": "28226279",
                "score": "93200",
                "nickname": "a飞龙飞",
                "head_image": "",
                "head_image_status": "0",
                "level": "5",
                "sex": "1",
                "video_price": 0, //视频价格
                "audio_price": 0 //语音价格
                "user_info": {
                    "uid":"1004170"
                    "user_nickname":"巴驰海"
                    "user_head_image":""
                    "user_head_image_status":"1"
                    "user_level":"27"
                    "user_sex":"1"
                }
            },
            ...
        ],
        "all_rank": [ //总榜
            {
                "user_id": "26392707",
                "score": "1499910",
                "nickname": "穷帅帅",
                "head_image": "",
                "head_image_status": "1",
                "level": "10",
                "sex": "1",
                "video_price": 0, //视频价格
                "audio_price": 0 //语音价格
                "user_info": {
                    "uid":"1004170"
                    "user_nickname":"巴驰海"
                    "user_head_image":""
                    "user_head_image_status":"1"
                    "user_level":"27"
                    "user_sex":"1"
                }
            },
            ...
        ]
    },
    "desc": ""
