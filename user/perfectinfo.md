### 用户完善资料完成注册接口

##### HTTP Method: POST
##### URL: https://host/app/user/perfectinfo.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
uid        |int| |true|   
session_id  |int| |true| 
job           |int| 职业 见配置文件|true|
education     |int| 学历 见配置文件|true|
income        |int| 月薪 见配置文件|true|
height        |int| 身高 具体数值(如170)|true|
marry         |int| 婚姻状态 见配置文件|true|
birthday|string| 生日|true|
weight|string| 体重 60kg|true|
bust|string| 罩杯|true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": { //用户信息
            id: "3",    //id
            nickname: "思考s",    //昵称
            head_image: "https://api.iofol.cn/public/upload/head_image/2016-04-28/3-1461826216.png",  //用户头像
            weixinId: "",  //openid，微信用户的唯一标识，也可以用来判断是否绑定微信号
            signature: "",    //个性签名
            phone: "",  //手机号
            sex: "1",   //性别1男，2女
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
            user_type: "1", //用户类型 0是普通用户 1是展示用户
            ext: {      //用户资料详情
                job: "1",   //职业
                education: "1", //学历
                birthday: "",   //生日
                weight: "",     //体重
                constellation: ""   //星座
                bust: "D"    //罩杯，男性则为空
            },
            version_code: "2.0.1",  //版本号
            qq_show: "0",   //0:qq对所有人显示 1:只对vip显示 2:对所有人都不显示
            phone_show: "0",    //0:手机对所有人显示 1:只对vip显示 2:对所有人都不显示
            online: "1", //0 不在线 1在线
            weixin: "", //微信
            weixin_show: "0"    //0:微信对所有人显示 1:只对vip显示 2:对所有人都不显示
            head_image_status: "0"  // 0:未上传头像 1:头像待审核 2:审核不通过 3:审核通过
            vip_buy_type: "2"  // 1: vip月卡   2：vip季度卡(季度vip)
        },
        "questions": {
        }
    },
    "desc": "完善资料成功"
}
```