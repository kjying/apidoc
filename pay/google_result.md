### google play支付验证

##### HTTP Method: GET
##### URL: https://host/app/pay/google_result.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
orderId|string||是|
packageName|string||是|
productId|string||是|
purchaseToken|string||是|


##### HTTP Response  H5支付
```json
{
	"code": 200,
	"data": {
	},
	"desc": ""
}
```