### 相片接口(上传、删除、查看、更改)

##### HTTP Method: POST
##### URL: https://host/app/user/photos.php

#####  Parameters（上传）
名称|格式|描述|必须|默认值
---|---|---|---|---
uid           | int ||true|
session_id| string ||true|
action|string |insert|true|
image        | file| 用户头像 HTTP上传|否|
image_url        | string| 七牛云的图片url|是|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "id": "7",  //相片id
            "thumb": "http://192.168.0.88:5656/public/upload/photo/user/thumb/000/000/001/thumb_572fe924e20fb.png"  //相片缩放图
            "path": "xxxxx"   //原图（如果是七牛云的话，该值跟thumb一样）
        }
    },
    "desc": "上传成功"
}
```
#####  Parameters（更改）
名称|格式|描述|必须|默认值
---|---|---|---|---
uid           | int ||true|
session_id| string ||true|
action|string |update|true|
image_url        | url| 七牛云的图片url（仅支持图片url方式）|是|
id|int |相片id|true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "id": "7",  //相片id
            "thumb": "http://192.168.0.88:5656/public/upload/photo/user/thumb/000/000/001/thumb_572fe924e20fb.png"  //相片缩放图
            "path": "xxxxx"   //原图（如果是七牛云的话，该值跟thumb一样）
        }
    },
    "desc": "更改成功"
}
```

#####  Parameters（删除）
名称|格式|描述|必须|默认值
---|---|---|---|---
uid           | int ||true|
session_id| string ||true|
action|string |delete|true|
id|int |相片id|true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1
    },
    "desc": "删除成功"
}
```

#####  Parameters（查看）GET
名称|格式|描述|必须|默认值
---|---|---|---|---
uid           | int ||true|
session_id| string ||true|
action|string |view|true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "limit_count":10,//图片上传数量限制
        "msg": [
            {
                "id": "6",  //相片id
                "uid": "1", //用户id
                "name": "572c5afdc00f1.png",  //相片名
                "path": "http://192.168.0.88:5656/public/upload/photo/user/000/000/001/572c5afdc00f1.png",  //相片原图
                "thumb": "http://192.168.0.88:5656/public/upload/photo/user/thumb/000/000/001/thumb_572c5afdc00f1.png",  //相片缩放图(固定尺寸)
                "ctime": "1462524669",  //上传时间
                "hits": "0",  //浏览数
                "status": "3"  //相片审核状态(1：待审核，2：审核不通过，3：审核通过)
            },
            {
                "id": "4",
                "uid": "1",
                "name": "572c56cfaeeb5.png",
                "path": "http://192.168.0.88:5656/public/upload/photo/user/000/000/001/572c56cfaeeb5.png",
                "thumb": "http://192.168.0.88:5656/public/upload/photo/user/thumb/000/000/001/thumb_572c56cfaeeb5.png",
                "ctime": "1462523599",
                "hits": "0",
                "status": "3"
            }
        ],
        "reward": {
            "reward_num": "21",  //我的相册打赏收入
            "reward_list": [     //机器人打赏列表
                {
                    "id": "10010066",  //机器人id
                    "nickname": "Ophelia", //昵称
                    "head_image": "http://192.168.1.89:81/public/upload/user/49.jpg?v=20160629",
                    "head_image_status": 3, //头像审核状态  仅为3(审核通过)的时候才显示头像
                    "aidou_num": 7  //获得爱豆数量
                },
                {
                    "id": "10010065",
                    "nickname": "小倩",
                    "head_image": "http://192.168.1.89:81/public/upload/user/48.jpg?v=20160629",
                    "head_image_status": 3,
                    "aidou_num": 7
                }
            ] 
        }
    },
    "desc": "加载成功"
}
```