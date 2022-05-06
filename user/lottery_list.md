### 抽奖列表

##### HTTP Method: GET
##### URL: https://host/app/user/lottery_list.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||

##### HTTP Response
```json
{
    code: 200,
    data: {
       result: 1,//1 获取成功 2 请先登录 5 抽奖功能未开启
       msg: {
            count:4//今日抽奖剩余次数
            reward：//奖品列表
            {
            type: "0", //0 礼物 1金币 2其他
            gift_id: "7", //礼物id
            num: 1,//数目
            name: "棒棒糖", //礼物名称
            photo_url: "http://leleimg.yewanhuyu.com/gift/2016-09-01_57c7a894b1bad.png", //图片url
            }，
           {
            type: 1, //0 礼物 1金币 2其他
            gift_id: 0, //礼物id
            num: 100,//数目
            name: "100金币", //礼物名称
            photo_url: "http://leleimg.yewanhuyu.com/gift/2016-09-01_57c7a900dfd9c.png", //图片url
           }, {
            type: "0", //0 礼物 1金币 2其他
            gift_id: "7", //礼物id
            num: 1,//数目
            name: "棒棒糖", //礼物名称
            photo_url: "http://leleimg.yewanhuyu.com/gift/2016-09-01_57c7a894b1bad.png", //图片url
            }，
           {
            type: 1, //0 礼物 1金币 2其他
            gift_id: 0, //礼物id
            num: 100,//数目
            name: "100金币", //礼物名称
            photo_url: "http://leleimg.yewanhuyu.com/gift/2016-09-01_57c7a900dfd9c.png", //图片url
           }, {
            type: "0", //0 礼物 1金币 2其他
            gift_id: "7", //礼物id
            num: 1,//数目
            name: "棒棒糖", //礼物名称
            photo_url: "http://leleimg.yewanhuyu.com/gift/2016-09-01_57c7a894b1bad.png", //图片url
            }，
           {
            type: 1, //0 礼物 1金币 2其他
            gift_id: 0, //礼物id
            num: 100,//数目
            name: "100金币", //礼物名称
            photo_url: "http://leleimg.yewanhuyu.com/gift/2016-09-01_57c7a900dfd9c.png", //图片url
           },{
            type: 1, //0 礼物 1金币 2其他
            gift_id: 0, //礼物id
            num: 100,//数目
            name: "100金币", //礼物名称
            photo_url: "http://leleimg.yewanhuyu.com/gift/2016-09-01_57c7a900dfd9c.png", //图片url
           }
    },
    desc: "获取成功"
}