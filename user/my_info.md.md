### 获取用户个人信息

##### HTTP Method: GET
##### URL: https://host/app/user/my_info.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||

##### HTTP Response
```json

{
    code: 200,
    data: {
            result: 1,  //0参数错误，1已登录，并返回用户信息，即msg，2未登录	
            task:{
                 user_lottery_switch:1 //抽奖开关
                 user_lottery_count：2 //抽奖剩余次数
                 user_sign_switch：1//签到开关
                 is_sign_today：1//今天是否已经签到过了
           }，
           visitor:{
               data:[
                   {
                       "id": "1001302",
                       "nickname": "毛泽西",
                       "head_image": "http:\/\/leleimg.yewanhuyu.com\/headImg_2018-07-05_.jpg__153075875538835.jpg",
                       "head_image_status": "3",
                       "vip": "1",
                       "user_type": "0",
                       "sex": "2",
                       "level": "8"
                    },
                    ...
                ],
                total: 7
            },
            msg: {	
                id: "3",    //id
                isNewUser：0//是否为新用户
                is_disturb：0//是否开启勿扰模式
                nickname: "思考s",    //昵称
                head_image: "https://api.iofol.cn/public/upload/head_image/2016-04-28/3-1461826216.png",  //用户头像
                head_image_new: "http://p8x3j9qoc.bkt.clouddn.com/headImg_2018-06-12_images_1000002_1528791721473.jpg",//用户上传的头像
                weixinId: "",  //openid，微信用户的唯一标识，也可以用来判断是否绑定微信号
                signature: "",    //个性签名
                phone: "",  //手机号
                sex: "1",   //性别1男，2女
                weixinId: "SDFSDFSDFS",   //微信openid
                age: "20",  //年龄
                session_id: "278848b9d7d7ee3867ef52b806347bb6", //session_id
                login_time: "1461814079",   //登录时间
                register_ip: "127.0.0.1",   //注册ip
                register_time: "1461813260",    //注册时间
                imei: "sdsdd4cxvkddw",
                is_binding: "0",    //是否绑定手机号0:未绑定手机；1：已绑定
                isdel: "0",     //是否删除，1删除，0未删除，2用户资料未完善
                vip: "0",   //vip等级0无vip
                height: "150",      //身高CM
                qq: "0",
                income: "1",    //月收入 1: 小于2000 2: 2000-5000 3: 5000-10000 4: 10000-20000 5: 20000以上
                marry: "1", //1:未婚 2:离异 3:丧偶
                province: "",   //省份
                city: "",   //城市
                origin_province：“”//家乡省份
                origin_city：“”//家乡城市
                user_type: "1", //用户类型 0是普通用户 1是展示用户
                ext: {      //用户资料详情
                    job: "1",   //职业
                    education: "1", //学历
                    birthday: "",   //生日
                    weight: "",     //体重
                    constellation: ""   //星座
                    bust："D" //女性罩杯，男性则为空

                },
                version_code: "2.0.1",  //版本号
                qq_show: "0",   //0:qq对所有人显示 1:只对vip显示 2:对所有人都不显示
                phone_show: "0",    //0:手机对所有人显示 1:只对vip显示 2:对所有人都不显示
                online: "1", //0 不在线 1在线
                weixin: "", //微信
                weixin_show: "0"    //0:微信对所有人显示 1:只对vip显示 2:对所有人都不显示
                head_image_status: "0"  // 0:未上传头像 1:头像待审核 2:审核不通过 3:审核通过
                vip_buy_type: "2"  // 1: vip月卡   2：永久vip
                gift_count: "900"  //单位（金币）。男性用户和女性主播都用这个字段
                "is_identity": 1  // -1:默认值，0已提交待审核，1审核通过成为主播，2审核不通过
                "alipay_id": "454554sf@qq.com"  //女性主播特有的支付宝账号
                "video_price": 1000 //女主播视频价格
                "audio_price": 1000 //女主播语音价格
                "star_rank":1//女主播星级
                "level": "10" //用户等级
                "auto_reply_status":0//女主播是否开启聊天托管
                "integral": "1100000" // 用户经验值
                "chat_key": "5000" // 用户邮票余额 
                "once_buy_gold": 1 // 用户是否曾买过金币，1是 2否。仅对非VIP男有用，相关字段：novip_male_gold_user_conn_enable
                "ext2": { //用户资料详情2
                    "phone_brand": "Redmi Note 3",
                    "network_state": 1,
                    "from": "1",
                    "imei": "e7c8dc8a01994ce38e548210f5efff2d",
                    "version_code": "79",
                    "channel": "test001",
                    "ip": "113.109.214.206",
                    "province": "广东",
                    "city": "广州"
                },
                "bank_name": "中国建设银行" // 银行名称 
                "bank_code": "105" // 银行代码 
                "bank_num": "" // 银行卡账号
                "bank_province": "广东" // 开户省/市
                "bank_city": "广州" //  开户地区
                "facebookId": "" //  facebook唯一标识码
                "googleId": "" //  Google 唯一标识码
                "facebook": "" //  Facebook账号
                "twitter": "" //  Twitter账号

            }

        },
    },
    desc: ""
}
```