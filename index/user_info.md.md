### 查看用户资料接口

##### HTTP Method: GET
##### URL: https://host/app/index/user_info.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
user_id  |int| 被访问人uid|true|
from     | string| 来路 该字段默认为空，如果是从"附近"跳转过来，需传from=nearby|true|
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
            "facebook": "", //facebook账号,
            "twitter": "", //Twitter账号
            "guard":{
                uid:1000001, // 用户id
                user_id:1000002, //主播id
                gold:10000, // 守护值
                status:1, // 状态 0守护过 1守护中
                nickname:"xxxxx", // 守护用户昵称
                head_image:'xxxxx', //守护用户头像
                level:1, // 用户等级
            }
        },
        "video": "",//最新免费视频
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
            },
         ],
         intimate: [ //亲密
            {
              user_id: "1002966",
              score: "30814",
              nickname: "濮阳浩言",
              head_image: "",
              head_image_status: "0",
              level: "18",
              sex: "1"
            },
            {
             user_id: "1001118",
             score: "15776",
             nickname: "测试用户1001118",
             head_image: "http://leleimg.yewanhuyu.com/headImg_2018-07- 
                          05_.jpg__153075875538835.jpg",
             head_image_status: "3",
             level: "15",
             sex: "1"
            },
            {
              user_id: "1001911",
              score: "8617",
              nickname: "indica",
              head_image: "http://leleimg.yewanhuyu.com/headImg_2018-08- 
                           17_images_1001910_1534495514700.jpg",
              head_image_status: "3",
              level: "14",
              sex: "1"
            },
            {
             user_id: "1003417",
             score: "3094",
             nickname: "石鸿朗",
             head_image: "",
             head_image_status: "1",
             level: "10",
             sex: "1"
            },
            {
              user_id: "1000026",
              score: "1312",
              nickname: "势光誉好腻害一直这样",
              head_image: "http://leleimg.yewanhuyu.com/headImg_2018-07- 
                           27_images_1000026_1532658453273.jpg",
              head_image_status: "3",
              level: "9",
              sex: "1"
           }
         ],
       gift: [ //礼物
          {
           total: 1757,
           list: [
            "http://sl.yiyuqipai.com/public/upload/gift/2016-09-01_57c7a900dfd9c.png",
            "http://sl.yiyuqipai.com/public/upload/gift/2016-09-01_57c7a894b1bad.png",
            "http://sl.yiyuqipai.com/public/upload/gift/2018-04-27_5ae30f9085c45.png",
            "http://sl.yiyuqipai.com/public/upload/gift/2016-12-18_585678835a465.png",
            "http://sl.yiyuqipai.com/public/upload/gift/2016-12-15_585258c6eee40.png"
            ]
         }
        ],
       evaluate: [ //主播形象
        {
         eid: "7",
         total: "120",
         content: "素颜美女",
         color: "#BE56E2"
        },
        {
         eid: "5",
         total: "98",
         content: "可爱",
         color: "#BE56E2"
        },
       {
        eid: "10",
        total: "78",
        content: "声音迷人",
        color: "#BE56E2"
       },
       {
        eid: "15",
        total: "68",
        content: "幽默风趣",
        color: "#BE56E2"
       },
       {
       eid: "4",
       total: "46",
       content: "妩媚撩人",
       color: "#BE56E2"
      },
      {
      eid: "8",
      total: "40",
      content: "火辣",
      color: "#BE56E2"
     },
     {
      eid: "9",
      total: "17",
      content: "成熟稳重",
      color: "#BE56E2"
     },
     {
      eid: "2",
      total: "12",
      content: "温柔体贴",
      color: "#BE56E2"
     },
     {
     eid: "19",
     total: "3",
     content: "多才多艺",
     color: "#BE56E2"
     }
    ],
   user_evaluate: [//用户评价
     {
      uid: "1002974",
      nickname: "莘良俊",
      head_image: "",
      data: [
        {
         content: "完美身材",
         color: "#FC8152"
        },
        {
         content: "成熟稳重",
         color: "#FF66AF"
        },
        {
        content: "火辣",
        color: "#5E8BF1"
        },
        {
        content: "完美身材",
        color: "#FC8152"
        },
        {
        content: "成熟稳重",
        color: "#FF66AF"
        },
        ,...
       ]
      },
      .....
    ]
    },
    "desc": ""
}
```