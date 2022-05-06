### 背包列表

##### HTTP Method: GET
##### URL: https://host/app/user/backpack.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||

##### HTTP Response
```json
{
    code: 200,
    data: {
       result: 1,//1 获取成功 2 请先登录 
       msg: {
            id: "1", //背包id
            uid: "1003597",
            type: "0", //0 礼物 1金币 2其他
            gift_id: "7", //礼物id
            num: 1,//数目
            name: "棒棒糖", //礼物名称
            photo_url: "http://leleimg.yewanhuyu.com/gift/2016-09-01_57c7a894b1bad.png", //图片url
            }，
           {
            id: "2", //背包id
            uid: "1003597",
            type: "0", //0 礼物 1金币 2其他
            gift_id: "8", //礼物id
            num: 1,//数目
            name: "棒棒糖2", //礼物名称
            photo_url: "http://leleimg.yewanhuyu.com/gift/2016-09-01_57c7a900dfd9c.png", //图片url
           }
    },
    desc: "获取成功"
}