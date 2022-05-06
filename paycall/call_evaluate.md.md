### 视频后评价主播

##### HTTP Method: post
##### URL: https://host/app/paycall/call_evaluate.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
call_id|int|通话id|false|
anchor_id|int|主播id|false|
eId|string|多个评价用英文逗号分开，例如 1,2,3|true|
type|int|0=>视频后评价主播 1=>新用户注册后选择的标签 |false|0

注意：客户端必须防止用户重复点击，防止重复提交数据
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1操作成功，2未登录 3 参数错误 
          msg:"操作成功"
    },
    desc: ""
}
