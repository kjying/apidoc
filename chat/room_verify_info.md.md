### 获取主播验证信息

##### HTTP Method: GET
##### URL: https://host/app/chat/room_verify_info.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int|用户id|是|
session_id|string|用户id|是|


##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "verify_status": "1", // 审核状态 0:未审核; 1:通过; 2: 拒绝
            "real_name": "myname2",
            "id_number": "410401199305160028",
            "image_url_1": "http://leleimg.yewanhuyu.com/identityImg_2019-09-14_images_0_1568468338486.jpg",
            "image_url_2": "http://leleimg.yewanhuyu.com/identityImg_2019-09-14_images_0_1568468408815.jpg",
            "image_url_3": " http://leleimg.yewanhuyu.com/identityImg_2019-09-14_images_0_1568468351450.jpg",
            "video_url": "http://leleimg.yewanhuyu.com/video_2019-09-14_video_0_1568468553680.mp4",
            "bank_name": "招商银行",
            "bank_num": "4392260088888888",
            "bank_province": "广东省",
            "bank_city": "广州市",
            "pic1_url": "",
            "pic2_url": "",
            "pic3_url": "",
            "pic4_url": "",
            "pic5_url": "",
            "pic6_url": ""
        }
    },
    "desc": ""
}
```