### 随机匹配

##### HTTP Method: GET
##### URL: https://host/app/paycall/match.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
type|int|1:视频 2:语音| 必传|

##### HTTP Response
```json
{
     "code": 200,
    "data": {
        "result": 1, // 1:匹配成功  2:未登录  0:匹配失败 3：金币不足
        "msg": {
            "user_id": "11213792",  //主播id
            "is_call_mass": 0, // 是否匹配到群发的主播  1：是  0：否，如果为1，下次call发起带上该参数
            "nickname": "嗯虐了", // 昵称
            "head_image": "http://tapi.hzjljs.com/public/upload/head_image/2017-09-14/11213792-1505388666.jpg?v=2", //头像
            "sex": "2", //性别， 2：女。只可能是女
            "type": 1, // 1：视频，2：语音
            "video_price": "200", //视频价格
            "audio_price": "100" //语音价格
        }
    },
    "desc": "匹配成功"
}
```