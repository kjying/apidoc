### 获取websocket链接ip

* 目的:用于方便socket服务的集群部署
* 如有返回ip, 客户端用ip来连接socket服务,否则用原先的域名.


##### HTTP Method: GET
##### URL: https://host/app/misc/ws.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||需有version_code,package,imei
hostname|string|客户端当前所用域名|是|

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "hostname": "xxx",      //原样返回
        "ip": "",               //如返回非空值 则用这个ip来连接
    },
    "desc": ""
}
```