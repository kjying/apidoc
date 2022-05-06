### 获取支付链接

##### HTTP Method: GET
##### URL: https://host/app/pay/pay_url.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
consume_type|int|session.php接口返回|是|
pay_type|int|0:未选择;1:支付宝;2:微信|否|0
order_from_type|int|1:私信礼物 2私信贵族 3私聊私密图片 4勿扰功能 5通话购买贵族 6通话购买金币 7首页购买金币 8 首页购买贵族 9 私信列表购买金币 10 我的页面购买金币 11 个人页微信购买贵族 12 我的页面购买贵族 13 微信购买金币 14 微信购买贵族 15 手机号购买金币 16 手机号购买贵族 17 QQ购买金币 18 QQ购买贵族 19 私密图片购买金币 20 私密图片购买贵族 21 私密视频购买金币 22 私密视频购买贵族 23 访客购买贵族 24 男用户个人资料购买贵族 25 帖子购买贵族 26 一键匹配购买金币 27 一键匹配购买贵族 28 选聊购买金币 29选聊购买贵族 30主播页购买金币 31主播页购买贵族 32砸蛋充值金币 33游戏购买金币 34守护购买金币 35购买公爵 36聊吧礼物购买金币 37直播间购买金币 38直播间购买贵族 39上麦购买金币|否|0
order_robot_id|int|产生订单时的来源主播id|否|0

##### HTTP Response  H5支付
```json
{
	"code": 200,
	"data": {
		"url": "http:\/\/api.mposbank.com\/papay\/wap_page.tran?out_trade_no=WTWAP8020180614000328829",
		"referer": "http:\/\/api.mposbank.com"
	},
	"desc": ""
}
```
##### HTTP Response  APP支付
```json
{
    "code": 200,
    "data": {
        "referer": "",
        "url": null,
        "url_params": {
            "Result": "SUCCESS",
            "appid": "wxdf4f282227c2a7d2",
            "nonce_str": "JEidgAwj43ICar4f",
            "partnerid": 1517775891,
            "prepay_id": "wx2616445745619637d846e38f2612653258",
            "sign": "D4666EBD2DC006FB447BB44E1A32085F",
            "timeStamp": 1543221897,
            "trade_type": "APP"
        }
    },
    "desc": ""
}
```
##### HTTP Response  小程序支付
```json
{
	"code": 200,
	"data": {
		"url": null,
		"url_params": {
			"mch_id": "26384828",
			"package_json": "{\"original_id\":\"gh_2373f7eeffa5\",\"app_id\":\"wx6ffe8fc3c7d5cd5f\",\"prepay_id\":\"909a5735c08d2815535369acf61c9128\"}",
			"prepay_id": "26802b37d80cb5f1c068302bf1428eae",
			"result_code": "SUCCESS",
			"return_code": "SUCCESS",
			"sign": "FD371EB6751D98E3902360D7A5724847",
			"trade_type": "trade.weixin.apppay2",
			"appid": "wx7ecd5e9701f3adaf"
		},
		"referer": "",
		"path": "pages\/index\/index?appId=wx6ffe8fc3c7d5cd5f&prepayId=909a5735c08d2815535369acf61c9128"
	},
	"desc": ""
}
```

##### HTTP Response  支付宝APP支付
```
{
    "code": 200,
    "data": {
        "path": "",
        "referer": "",
        "sdk_type": "alipay_app",
        "url": "alipay_sdk=alipay-sdk-php-20161101&amp;app_id=2016022901170484&amp;biz_content=%7B++++%22subject%22%3A%22%E5%85%85%E5%80%BC-%E6%8A%95%E8%AF%89%E4%B8%8E%E5%AE%A2%E6%9C%8Dqq%3A+2892581156%22%2C++++%22out_trade_no%22%3A%222019080120070150600311%22%2C++++%22total_amount%22%3A0.98%2C++++%22product_code%22%3A%22QUICK_MSECURITY_PAY%22++%7D&amp;charset=UTF-8&amp;format=json&amp;method=alipay.trade.app.pay&amp;notify_url=http%3A%2F%2Fsl.yiyuqipai.com%2Fapp%2Fpay%2Falipay%2Fcallback_alipay.php&amp;sign_type=RSA2&amp;timestamp=2019-08-01+20%3A07%3A01&amp;version=1.0&amp;sign=dkVVCbgIaC2XeE84GVqNQJRMtmEnlIjgMeB78BfJSi7Ckh1R8%2BeK2T6LZ7lezsQ6ox8I7gbatzkmou8entxNRhEzn2vtId80qevk1XMUG7tN3tiwll39pt37wBJidKCBN%2BVQQPJGlI%2B8KmsV2Dci3BvjeHfHOZrW%2Fd6HR3zRkXgOiYvsLxhbM5DvXqPXSiTCgLxZsS77xgdTC%2Fw3JwG%2BC42AIIW%2Fa78i7KjdpfSMZoE93T2r2mrSImKf9S7iLlIaUAv5Kg8UZmroH8tEO0FNYgKP3l0zinaRc0DLlQAstwsNotX9OAGdXwKv%2Bm3yfSfY%2FfJN6MOL7vzZ76Ke6x9M5w%3D%3D",
        "url_params": ""
    },
    "desc": ""
}
```

* 如referer为空则不需要设置Referer