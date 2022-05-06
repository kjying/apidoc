### 初始化客户端

##### HTTP Method: GET
##### URL: https://host/app/user/session.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||

##### HTTP Response
```json

{
    code: 200,
    data: {
        bank: [ //印象标签
         '中国建设银行','中国农业银行',...
        ],
        evaluate: [ //印象标签
          {
           id: "1", //印象id
           type: "0",  // 类型 0 好评 1坏评
           content: "性感", //内容
           color: "#BE56E2", //底色
           status: "1" //状态 1开启 0关闭
          },
          {
          id: "2",
          type: "0",
          content: "温柔体贴",
          color: "#BE56E2",
          status: "1"
        },
        ....,
        ]
        "small":{
            "small_download_switch":1 //小程序下载页面开关
            "app_download":''//
            "small_share_title":''//分享标题
            "small_share_photo":''//分享图片
            "small_share_url":'pages/splash/splash'//分享url
         "small_share_download_url":'http://wlele.yewanhuyu.cn/activity/download/leliao'//分享下载url
            "small_recharge_switch":0//小程序充值开关
        }
        "other":{
            "recharge_list_switch":1//跑马灯开关
            "call_mass_login_time"：60//用户登录之后开始收到脚本、托管和群拨CD,即用户冷却时间
             user_lottery_switch:1 //抽奖开关
             user_sign_switch：1//签到开关
             match_switch：1//一键匹配开关
             match_gift_count：1000//一键匹配金币数值
             weixin_gift_count：9800//微信查看收费金币
             phone_gift_count：9800//手机号查看收费金币
             qq_gift_count：9800//QQ查看收费金币
             video_gift_count：100//私密视频收费金币
             photo_gift_count：100//私密图片收费金币
             choose_chat：0//选聊开关 0关闭 1开启
             default_tab：0//发现页默认tab 1推荐 2热门 3选聊
             automatic_multicast：0//自动群拨CD
             is_family：0//打包家族 0否 1是
             bisexual_switch：0//两性论坛开关 0关闭 1开启
             notice_content：''//公告
             notice_url：''//公告跳转地址
             each_gold: 2000 // 每次增加金额
        }
        "game":{      //游戏
             smash_eggs_switch: 1 // 砸蛋开关 0关闭 1开启
             chat_switch: 1 // 文字聊天开关 0关闭 1开启
             game_switch: 1 // 游戏总开关 0关闭 1开启
             chat_level_switch: 0 // 聊天等级限制
         }
        "noble":{
           "phone_fare_switch":1//充值送话费开关
           "vip_send_gold":666//送金币
           "vip_send_phone_fare":50//送话费
           "noble_banner_fare_url"=>'http://leleimg.yewanhuyu.com/banner/2019-01-16_1547625699.png'
           "noble_banner_gold_url"=>'http://leleimg.yewanhuyu.com/banner/2019-01-16_1547624589.png'
        }
        "delete_script":{      //过期脚本消息
            "delete_script_switch":1  //开关
            "delete_script_timer_hour":24 //设置过期小时数
         }
        "extension":{
          "extension_division_man":0.2//男版充值金币推广分成
          "extension_division_woman":0.1//女版充值金币推广分成
        }
        "share":{
         "share_title":''//分享标题
         "share_desc":''//分享简介
         "share_photo":''//分享图片
         "share_url":''//分享url
        }
        "script":{
           "timer_min":120 //客户端轮询时间间隔最小值 单位 秒
           "timer_max":180 //客户端轮询时间间隔的最大值 单位 秒
           "read_max_num":12//脚本和托管未读消息的上限条数
        }
        "trusteeship":{
           "behavior_trusteeship_switch":1 //v2.4 行为托管开关
           "behavior_trusteeship_timer_min":10//v2.4 客户端行为托管时间间隔最小值 单位 秒
           "behavior_trusteeship_timer_max":30//v2.4 客户端行为托管时间间隔最大值 单位 秒
        }
        "call":{
           "call_force_vip":1 //通话是否强制vip
           "free_video_switch":1//免费通话开关
           "call_mass_client_timer":30//客户端接收群拨时间间隔 秒
           "call_mass_client_num":1//客户端接收群拨条数限制
           "call_mass_client_max_num":1000 //  每日客户端接收群拨条数限制
           "click_num_cancel":3//免费视频 点击次数取消按钮
           "behavior_call_mass_switch":1//v2.4 行为群拨开关
           "behavior_call_mass_timer":60//v2.4 行为群拨时间间隔 单位 秒
           "free_video_time": 30 // 免费通话时间
        }
        "firstGift": {
            "firstGift": {    //首次礼物信息
                "count": 1,
                "ctime": "1507533843",
                "id": "1",
                "img": "http://seeklove.momohuyu.com/public/upload/gift/2016-09-01_57c7a894b1bad.png",
                "name": "\u68d2\u68d2\u7cd6",
                "price": "10",
                "status": "0"
            },
            "sendToUsers": [    //已经送过礼物的用户id列表
                "1001366",
                "1000011"
            ],
            "active": 0,   //0:功能关闭; 1:功能开启
            "force_vip": 0,   //首次礼物强制VIP开关 0:功能关闭; 1:功能开启
            "fare_num":5 //免费发送信息条数
            "total_num":10 //当前用户发送普通信息的条数
        },
        verify: 1,  //1 过申，0正常
        login: {
            result: 1,  //0参数错误，1已登录，并返回用户信息，即msg，2未登录，3该用户已经被删除，4资料未完善 5未绑定手机 7.190版本女性未实名验证 8.270版本男性用户未选择标签 
            send_list: {1,2,3}//加上socket之后，向socket请求send接口	
            msg: {	
                id: "3",    //id
                register_call_force_vip：1 //v2.2版本 注册时通话是否强制vip
                isNewUser：1//是否为新用户
                get_free_video：1//是否拥有免费通话
                noble：1//是否为贵族
                noble_over_time：2018-12-12//贵族到期时间
                noble_consume_type：21//贵族续费类型
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
                "already_buy_gold": 1 // 用户是否曾买过金币，1是 2否。
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
                "facebookId": "" //  facebook唯一标识码
                "googleId": "" //  Google 唯一标识码
                "facebook": "" //  Facebook账号
                "twitter": "" //  Twitter账号

            }

        },
        info_config: {  //配置信息
            "pay_price": {  //充值页面配置信息
                "vip": [    //vip配置
                    {
                        "title": "永久VIP(开通送150元话费)",    //标题
                        "goods_count": "90",    //vip天数
                        "price": "520",     //价格
                        "discount_price": "188",    //折扣价格
                        "consume_type": 3,  //类型
                        "tag_value": "抢购",   //购买bottom
                        "sub_title": "开通送100元话费"  //副标题(新加字段)
                        'send_good'=>'3000',//送金币
                        "send_phone_fare"=>'50'//送话费 单位 元
                        "display": 0 //0显示，1隐藏
                        'default_select'=>1,//默认选中
                    },
                    {
                        "title": "半年vip",
                        "goods_count": "30",
                        "price": "138",
                        "discount_price": "68",
                        "consume_type": 2,
                        "tag_value": "抢购",
                        "sub_title": "3",
                        'send_good'=>'1000',//送金币
                        "send_phone_fare"=>'50'//送话费 单位 元
                        "display": 0
                    },
                    {
                        "title": "试用VIP(3天VIP)",
                        "goods_count": "3",
                        "price": "100",
                        "discount_price": "2",
                        "consume_type": 1,
                        "tag_value": "试用"
                    }
                ],
                "gold":[ //金币配置
                    {
                        "title": "1050金币",
                        "goods_count": "1050",
                        "price": "",
                        "discount_price": "100", //实际价格
                        "consume_type": 4,
                        "tag_value": "抢购",
                        "sub_title": "赠送50金币",
                        "display": 1,
                        "send_good":1000，
                        'default_select'=>1,//默认选中
                    },
                    {
                        "title": "500金币",
                        "goods_count": "500",
                        "price": "",
                        "discount_price": "50",
                        "consume_type": 5,
                        "tag_value": "抢购",
                        "sub_title": "无优惠",
                        "display": 1
                    },
                    {
                        "title": "100000金币",
                        "goods_count": "100000",
                        "price": "",
                        "discount_price": "0.01",
                        "consume_type": 6,
                        "tag_value": "抢购",
                        "sub_title": "无优惠",
                        "display": 1
                    }
                ]
                "apple_gold":[ //苹果内购金币配置
                    {
                        "title": "1050金币",
                        "goods_count": "1050",
                        "price": "",
                        "discount_price": "100", //实际价格
                        "consume_type": 4,
                        "tag_value": "抢购",
                        "sub_title": "赠送50金币",
                        "display": 1
                    },
                    {
                        "title": "500金币",
                        "goods_count": "500",
                        "price": "",
                        "discount_price": "50",
                        "consume_type": 5,
                        "tag_value": "抢购",
                        "sub_title": "无优惠",
                        "display": 1
                    },
                    {
                        "title": "100000金币",
                        "goods_count": "100000",
                        "price": "",
                        "discount_price": "0.01",
                        "consume_type": 6,
                        "tag_value": "抢购",
                        "sub_title": "无优惠",
                        "display": 1
                    }
                ]
                "aidou": [   //鲜花配置
                    {
                        "title": "购买880爱豆(活动期间打折)",
                        "goods_count": "880",
                        "price": "88",
                        "discount_price": "78",
                        "consume_type": 8,
                        "tag_value": "抢购"
                    },
                    {
                        "title": "购买600爱豆(活动期间打折)",
                        "goods_count": "600",
                        "price": "60",
                        "discount_price": "56",
                        "consume_type": 7,
                        "tag_value": "抢购"
                    }
                ],
                "scroll": [
                    '[[昵称]]成为了永久vip，获得了100元话费',
                    '购买vip，[[昵称]]获得50多鲜花'
                ],
                "setting": {
                    "tel_fare": "50"
                }
            },
            "spread_app": [
                {
                    "app_name": "夜色",
                    "app_url": "http://down.95xiu.com/95show.apk"
                },
                {
                    "app_name": "95秀",
                    "app_url": "http://down.95xiu.com/95show.apk"
                }
            ],
            'hit_rate': {
                'say_hello': 50,    //say_hello 打招呼后，有多少几率回复
                'random_say_hello': 40,    //random_say_hello: 多少几率触发随机打招呼
                'chat_again': 60   //chat_again：玩家回复后，机器人有多少几率回复
                'interval_time':15    //interval_time 回复聊天时间间隔
                'poll_chat_rate_incre': 2,  //定时消息概率递增量
                'poll_chat_rate_decre': 25, //定时消息概率递减量
                'poll_max_chat_rate': 80,   //定时消息概率最大值
                'poll_min_chat_rate': 2 //定时消息概率最小值
                'max_geo_msg_count': 3 //最大地标信息数
                'voice_chat_rate': 30 //除4（用户回复后）外的场景，有多少概率请求语音消息(0~100)30
             },
            'limit_register': {
                'man': 2,   //1限制男注册，2不限制
                'woman': 1  //1限制女注册，2不限制
            },
            'limit_geo':{
                'poitype':'政府机构|购物;家电数码|购物;家居建材',    //父类型
                'tag':'汽车服务|公司企业|政府机构' //子类型
            },
            "pay_switch": "1",   //1使用妙讯微信支付，2使用梓微兴微信支付
            "custom_service": {
                "switch1": "1", //switch1价格列表
                "switch2": "1", //switch2订单支付方式选择
                "qq": "935756165"
            },
            "money_back": {     //领取话费
                "type": "1",    //领取话费提示方案，1、30天后领取，2、每天领取300数量限制
                "alert_text1": "成为VIP30天后才可领取话费",     //第一次弹窗提示
                "alert_text2": "您的请求已接受，话费将在7天内到帐，若未到帐，请再次领取"   //第二次弹窗提示
            },
            "cleaning": {
                "clean_status": 1, // 1表示处于清理状态  0表示处于正常运营状态
                "clean_ver": 1  // 累积清理序号，服务器每次手动+1
            },
            "alarm": {
                "h5_text": '会员特权：趣味小游戏 点击进入>>',
                "alarm_text": '此用户发布疑似诈骗信息，请注意财产安全',
                "ids": '10010073,10010828'  //被标记的有诈骗嫌疑的用户id,
                "status": "1", // 0关闭  1开启 
                "url": "http://image.iofol.cn/new_html/help_center/safe_center.html" //安全交友链接
            },
            "tipoff":{
                "status": "0" //0关闭  1开启 2VIP后开启
            },
            "complain":{
                "status": "0" //0关闭  1开启 2VIP后开启
            },
            "h5_game":{
                "status": "0" //0关闭  1开启 
            },
            "tax_rate": 0.1  //主播提现所得税率
            "gift_divide_rate": 0.4  //收礼方礼物价值分成比例
            "gold_ratio": 100 // 汇率，100金币=1元"
            "gold_photo": 100 // 私密图价格
            "gold_limit": 500000  //金币上限值，当用户金币数大于此值时不允许充值金币
            "single_message_cost": 10 //发送单条信息花费金币
            "refresh_interval": 20 //客户端最小刷新时间间隔(秒)
            "activity_intro_rank_url": "http://api.hzjljs.com/public/html/about_level/index.html"//个人中心里的"说明"按钮，客户端请加上性别参数sex=1(1男，2女)，到该url后面。如xxx.html?sex=1
            "novip_male_gold_user_conn_enable": 1 // 购买过金币的非vip男用户，连接im的开关，和once_buy_gold有关。1打开，0关闭
            "guild_bind_phone_after_consume": 1 //充值后绑定手机引导的开关。1打开，0关闭
            "vip_privilege": { //vip 特权
                "chat": "1",
                "see_photo": "1",
                "see_more_visitor": "1",
                "see_more_follow": "1",
                "video_call": "1",//视频聊天
                "audio_call": "1"//语音聊天
            },
        }
    },
    desc: ""
}
```