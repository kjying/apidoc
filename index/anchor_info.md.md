### 查看用户资料接口

##### HTTP Method: GET
##### URL: https://host/app/index/anchor_info.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
user_id  |int| 被访问人uid|true|
page  |int| 推荐列表页数|true| 1
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {       //原样输出
            "origin_place":‘广东广州’ //家乡
            "connection_rate":80%  //接通率
            "connection_num":80 //人数
            "connection_time":80 //时长 分钟
            "video_num":5 //视频数量
            "fans": 2,         //关注数
            "is_concern": 0,   // 0表示未关注，1表示已关注，2表示隐藏关注图标(自己访问自己)
            "head_image": "",
            "id": 1011,
            "nickname": "别说话快快吻我",
            "photo_num": "0",   //相片数
            "login_time": "2016-05-20 13:49:49",
            "purpose": "",   //交友目的
            "idea": "",      //恋爱观念
            "hope": "",      //首次见面希望
            "hope_place": "",  //喜欢爱爱的地点
            "want_age": "不限",  //征友条件年龄
            "want_place": "不限",
            "want_height": "不限",
            "want_education": "不限",
            "want_income": "不限",
            "sex": "男",
            "age": "24岁",
            "place": "广东 广州",
            "height": "168cm",
            "income": "20000以上",
            "marry": "未婚",
            "education": "硕士及以上",
            "job": "政府机关/事业单位工作者",
            "constellation": "处女座",
            "weight": "65-70(kg)",
            "birthday": "1992-09-22",
            "qq": "123456",
            "phone": "保密",
            "weixin": "仅钻石vip可见",
            "distance": "7.87km",
            "bust": "D", //D罩杯,
            "vip": 0  // 0表示非VIP 1表示VIP
            "is_identity": 1 // 默认-1, 1表示为已认证主播
            "status": -1  //  默认-1，-1表离线，0表通话中，1表空闲
            "accept_video": 1  // 1接收视频，0不接受。可以无视此字段
            "accept_audio": 1  // 1接收语音，0不接受。可以无视此字段
            "video_price": 1000  // 视频价格
            "audio_price": 1000  // 语音价格
            "enable_call": 1 // 1表示男号能通话，0表示不能
        },
        "video": "",//点赞最高免费视频
        "photos": [
            {
                "id": "4275",
                "uid": "10010025",
                "path": "http://img.kaconshop.com/upload/photo/user_f/path/23.jpg?v=2",
                "thumb": "http://img.kaconshop.com/upload/photo/user_f/thumb/23.jpg?v=2",
                "visible": 1,    //1不模糊处理，0模糊处理
                "is_recommend": 0    //1是私密图片，0否
            },
            {
                "id": "4276",
                "uid": "10010025",
                "path": "http://img.kaconshop.com/upload/photo/user_f/path/24.jpg?v=2",
                "thumb": "http://img.kaconshop.com/upload/photo/user_f/thumb/24.jpg?v=2",
                "visible": 1,
                "is_recommend": 0
            },
            {
                "id": "4277",
                "uid": "10010025",
                "path": "http://img.kaconshop.com/upload/photo/user_f/path/25.jpg?v=2",
                "thumb": "http://img.kaconshop.com/upload/photo/user_f/thumb/25.jpg?v=2",
                "visible": 1,
                "is_recommend": 0
            }
         ]
    },
    "desc": ""
}
```