### 用户消息推送用户行为通知接口

##### HTTP Method: GET
##### URL: https://host/app/push/action_notify.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
token    | string |友盟消息推送服务对设备的唯一标识||
status       | int |当切换到后台或者直接杀进程, 请求status=1；当切回到前台，请求status=0|true|
package      | string |包名|true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1    //1 成功
    },
    "desc": ""
}
```