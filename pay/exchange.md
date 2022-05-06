### 金币与秀币兑换

##### HTTP Method: GET
##### URL: https://host/app/pay/exchange.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数|||是|
amount|int|数量|是|
exchange_type|int|1:金币兑换秀币;2:秀币兑换金币|否|1

##### HTTP Response
```json
{'code': 200, 'data': {'result': 1}, 'desc': '兑换成功'}
```

##### HTTP Error Response
```json
{'code': 200, 'data': {'result': 2}, 'desc': '请先登录'}
{'code': 200, 'data': {'result': 3}, 'desc': '数量错误'}
{'code': 200, 'data': {'result': 4}, 'desc': '金币不够'}
{'code': 200, 'data': {'result': 5}, 'desc': '兑换失败'}
```
