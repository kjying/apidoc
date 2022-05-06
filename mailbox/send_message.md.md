### 用户发送消息接口

##### HTTP Method: get
##### URL: https://host/app/mailbox/send_message.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid           | int ||true|
session_id| string ||true|
type        | int| 消息类型，4用户回复之后机器人回复， 25 主播设置聊天托管后，自动向新用户推送消息；26 主播设置聊天托管后，自动回复用户消息；) |true|
user_id      | int  | 接受用户uid -1时对随机一个用户发消息|true|
msg_type   | int | 1机器人消息,2用户发送的消息|true|
content    | string |消息内容|true|
content_type   | int |1文本消息，2语音消息,3图片消息|true|
sid         |int |声源id|true|
sids         |string |客户端已有的声源id列表(如 "1,2,3,4,5")|true|
gid         |int| 套路id|true|
gids         |string |客户端已有的套路id列表(如 "1,2,3,4,5")|true|
g_type         |int |要请求的套路步骤|true|
novip_guide    |int| 非会员引导，1表示(需要引导)客户端未记录过，0表示(不再需要引导)记录过|true|
yids         |string |客户端已有的纯文本、带礼物图的索礼消息m_id集合(如 "1,2,3,4,5")|true|
pids         |string |客户端已有的相片索礼消息pid(在sys_demand_gift下)集合(如 "1,2,3,4,5")|true|
##### HTTP Response
```json
{
    code: 200,
    data: {
        result: 1,  //1已登录，2未登录,3消息体msg为空
        msg: {
            m_id:1,     //消息的id  (如果返回content_type为1或8，需将m_id保存，下次以yids上传)
            message: "http://192.168.0.163:82/public/upload/audio/578d98a10693b.mp3", //消息内容，语音消息为语音链接
            time: 1469083136,   //时间戳
            content_type: 2,    //1文本消息(纯文本索礼消息也是此类型)，2语音消息 3图片消息, 7相片索礼消息(废弃)  8带礼物图的索礼
            sid: 2,             //声源id  （文本消息固定值为0）
            c_code: "0",    //语音消息的内容标记
            type: 6,    //消息场景  (7表示非付费引导回复, 9表示所有的系统索礼消息，要记录到客户端)
            contact_type: 1,    //联系方式的类型，0非联系方式消息，1qq，2微信，3手机号
            audio_time: 0,      //语音时长（秒）
            gid: 2,     //套路id（非套路消息是0）
            g_type: 7,  //下次请求套路的步骤（非套路消息是0）
            g_interval: 7, //下次请求套路的时间（非套路消息是0）
            user_info: {    //发送机器人用户信息
                id: "10011471",
                nickname: "汝勿离",
                head_image: "http://192.168.0.163:82/public/upload/head_image/2016-07-08/tb_7903-1467945103.jpg?v=20160629",
                vip:0,   //0非vip，1vip
                sex: "2"   //性别，1男，2女
                user_type: "0"   //0真实用户，1机器人
                enable_call: 1 //1表示对方能使用视频语音通话，0表示不能
                video_price: 0 // 视频价格，金币
                audio_price: 0 // 语音价格，金币
                gift_count: 300 //金币
            },
            "gift_count": "400",  //金币余额，当msg_type=2（用户发送消息），且result=1时有返回
            "chat_key": "5000",  //邮票余额，当msg_type=2（用户发送消息），且result=1时有返回
            "sys_demand_gift": { //系统索礼消息。sys_demand_gift只有在content_type=7时才有返回
                "pid": 1,  // 方案id，男性点击送礼的时候，要带上这个参数
                "content": // 自定义文字
                "photos": [ // 相片url集合
                    "xxxx",
                    "xxxx",
                ] 
                "gid": 2  // 礼物id
                "g_num": 10 // 礼物数量
                "g_img": "xxxx" //礼物图标
                "g_price": 100  //礼物单价，金币
                "g_name": "大钻石"  //礼物名称
            }
            "sys_demand_gift_2":{ // sys_demand_gift_2仅在content_type=8时才有返回
                    "content": "可以送我玫瑰吗" //文字
                    "gid": 1  //礼物id
                    "g_num": 20 //礼物数量
                    "g_img": "xxxx"  //礼物图标
                    "g_price": 100  //礼物单价，金币
                    "g_name": "大钻石"  //礼物名称
            }
        },
        "cleaning": {
            "clean_status": 1, // 1表示处于清理状态  0表示处于正常运营状态
            "clean_ver": 1  // 累积清理序号，服务器每次手动+1
        }
    },
    desc: ""
}
```