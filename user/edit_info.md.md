### 修改个人资料接口

##### HTTP Method: POST
##### URL: https://host/app/user/edit_info.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
signature     | string |个人签名 | true|
nickname      | string |昵称| true|
origin_province      | string |家乡省份 如"山西"|true |
origin_city          | string |家乡城市 如"太原"|true |
height        | string |身高 如"175"|true |
income        | int    |收入 如1 见配置文件| true|
marry         | int    |婚姻 如1 见配置文件|true |
qq            | string |qq   |true |
qq_show       | int    |0:对所有人显示 1:只对vip显示 2:对所有人都不显示|true |
phone         | string |电话| true|
phone_show    | int    |0:对所有人显示 1:只对vip显示 2:对所有人都不显示|true |
weixin        | string |微信| true|
weixin_show   | int    |0:对所有人显示 1:只对vip显示 2:对所有人都不显示|true |
education     | int    |学历 如1 见配置文件|true |
job           | int    |职业 如1 见配置文件|true |
birthday      | string |生日 如"1992-09-22" 请用这种时间格式| true|
weight        | int    |体重 如1 见配置文件| true|
bust          | string |胸围 例如：D| true|
facebook      | string |Facebook账号| true|
twitter       | string |Twitter账号| true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,
        "msg": {
            "id": "3",
            "nickname": "思考s",
            "head_image": "",
            "signature": "what",
            "phone": "13794305519",
            "sex": "1",
            "age": "20",
            "session_id": "278848b9d7d7ee3867ef52b806347bb6",
            "login_time": "1462326375",
            "register_ip": "127.0.0.1",
            "register_time": "1461813260",
            "imei": "sdsdd4cxvkddw",
            "is_binding": "0",
            "isdel": "0",
            "vip": "0",
            "height": "165",
            "qq": "0",
            "income": "2",
            "marry": "2",
            "province": "广东省",
            "city": "深圳市",
            "origin_province": "广东省",//家乡
            "origin_city": "深圳市",//家乡
            "user_type": "1",
            "ext": {
                "job": "2",
                "education": "2",
                "birthday": "1989-03-07",//生日
                "weight": "3",
                "constellation": "2", //星座
                "bust": "D"
            },
            "version_code": "2.0.1",
            "qq_show": "0",
            "phone_show": "0",
            "online": "1",
            "weixin": "",
            "weixin_show": "0",
            "head_image_status": "0",
            "vip_buy_type": "2",  // 1: vip月卡   2：vip季度卡(季度vip)
            "facebook": "",
            "twitter": ""
        }
    },
    "desc": "修改资料成功"
}