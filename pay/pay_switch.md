### 支付方式

##### HTTP Method: GET
##### URL: https://host/app/pay/pay_switch.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
switch_from|int|0:金币;1:vip|是|

* switch_from=0时返回gold_prices  switch_from=1时返回vip_prices

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "pay_menu": [
            {
                "desc": "\u652f\u4ed8\u5b9d",
                "gold_prices": [
                    {
                        "consume_type": 3,
                        "default_select": 0,
                        "discount_price": "48",
                        "display": 0,
                        "goods_count": "4320",
                        "price": "",
                        "send_good": "0",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "4320\u91d1\u5e01"
                    },
                    {
                        "consume_type": 4,
                        "default_select": 1,
                        "discount_price": "98",
                        "display": 0,
                        "goods_count": "8820",
                        "price": "",
                        "send_good": "488",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "8820\u91d1\u5e01"
                    },
                    {
                        "consume_type": 5,
                        "default_select": 0,
                        "discount_price": "168",
                        "display": 0,
                        "goods_count": "15120",
                        "price": "",
                        "send_good": "718",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "15120\u91d1\u5e01"
                    },
                    {
                        "consume_type": 6,
                        "default_select": 0,
                        "discount_price": "398",
                        "display": 0,
                        "goods_count": "35820",
                        "price": "",
                        "send_good": "1088",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "35820\u91d1\u5e01"
                    },
                    {
                        "consume_type": 7,
                        "default_select": 0,
                        "discount_price": "998",
                        "display": 0,
                        "goods_count": "89820",
                        "price": "",
                        "send_good": "2688",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "89820\u91d1\u5e01"
                    },
                    {
                        "consume_type": 8,
                        "default_select": 0,
                        "discount_price": "2998",
                        "display": 0,
                        "goods_count": "269820",
                        "price": "",
                        "send_good": "10588",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "269820\u91d1\u5e01"
                    }
                ],
                "pay_type": 1,
                "show": 1
            },
            {
                "desc": "ApplePay",
                "gold_prices": [
                    {
                        "consume_type": 3,
                        "default_select": 0,
                        "discount_price": "6.99",
                        "display": 0,
                        "goods_count": "3425",
                        "price": "",
                        "product_id": "com.secretLook.chat7",
                        "send_good": "0",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "3425\u91d1\u5e01"
                    },
                    {
                        "consume_type": 4,
                        "default_select": 1,
                        "discount_price": "13.99",
                        "display": 0,
                        "goods_count": "6855",
                        "price": "",
                        "product_id": "com.secretLook.chat15",
                        "send_good": "488",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "6855\u91d1\u5e01"
                    },
                    {
                        "consume_type": 5,
                        "default_select": 0,
                        "discount_price": "23.99",
                        "display": 0,
                        "goods_count": "11755",
                        "price": "",
                        "product_id": "com.secretLook.chat24",
                        "send_good": "718",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "11755\u91d1\u5e01"
                    },
                    {
                        "consume_type": 6,
                        "default_select": 0,
                        "discount_price": "59.99",
                        "display": 0,
                        "goods_count": "29395",
                        "price": "",
                        "product_id": "com.secretLook.chat52",
                        "send_good": "1088",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "29395\u91d1\u5e01"
                    },
                    {
                        "consume_type": 7,
                        "default_select": 0,
                        "discount_price": "149.99",
                        "display": 0,
                        "goods_count": "73495",
                        "price": "",
                        "product_id": "com.secretLook.chat66",
                        "send_good": "2688",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "73495\u91d1\u5e01"
                    },
                    {
                        "consume_type": 8,
                        "default_select": 0,
                        "discount_price": "399.99",
                        "display": 0,
                        "goods_count": "195995",
                        "price": "",
                        "product_id": "com.secretLook.chat80",
                        "send_good": "10588",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "195995\u91d1\u5e01"
                    }
                ],
                "pay_type": 3,
                "show": 1
            },
            {
                "desc": "GooglePay",
                "gold_prices": [
                    {
                        "consume_type": 3,
                        "default_select": 0,
                        "discount_price": "6.99",
                        "display": 0,
                        "goods_count": "3425",
                        "price": "",
                        "product_id": "com.secretLook.chat7",
                        "send_good": "0",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "3425\u91d1\u5e01"
                    },
                    {
                        "consume_type": 4,
                        "default_select": 1,
                        "discount_price": "13.99",
                        "display": 0,
                        "goods_count": "6855",
                        "price": "",
                        "product_id": "com.secretLook.chat15",
                        "send_good": "488",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "6855\u91d1\u5e01"
                    },
                    {
                        "consume_type": 5,
                        "default_select": 0,
                        "discount_price": "23.99",
                        "display": 0,
                        "goods_count": "11755",
                        "price": "",
                        "product_id": "com.secretLook.chat24",
                        "send_good": "718",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "11755\u91d1\u5e01"
                    },
                    {
                        "consume_type": 6,
                        "default_select": 0,
                        "discount_price": "59.99",
                        "display": 0,
                        "goods_count": "29395",
                        "price": "",
                        "product_id": "com.secretLook.chat52",
                        "send_good": "1088",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "29395\u91d1\u5e01"
                    },
                    {
                        "consume_type": 7,
                        "default_select": 0,
                        "discount_price": "149.99",
                        "display": 0,
                        "goods_count": "73495",
                        "price": "",
                        "product_id": "com.secretLook.chat66",
                        "send_good": "2688",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "73495\u91d1\u5e01"
                    },
                    {
                        "consume_type": 8,
                        "default_select": 0,
                        "discount_price": "399.99",
                        "display": 0,
                        "goods_count": "195995",
                        "price": "",
                        "product_id": "com.secretLook.chat80",
                        "send_good": "10588",
                        "sub_title": "",
                        "tag_value": "\u62a2\u8d2d",
                        "title": "195995\u91d1\u5e01"
                    }
                ],
                "pay_type": 4,
                "show": 1
            }
        ],
        "pay_switch": 1
    },
    "desc": ""
}
```


##### 说明
* 显示弹窗时按pay_menu的desc显示且仅显示show=1的项目