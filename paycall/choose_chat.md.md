### 选聊

##### HTTP Method: GET
##### URL: https://host/app/paycall/choose_chat.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1, // 1成功  2未登录 3网络错误
        "total": 0,  // 在线可视频s级主播数量
        "video": [
            "http:\/\/leleimg.yewanhuyu.com\/video\/2019-04-23_1556008530.mp4",
            "http:\/\/leleimg.yewanhuyu.com\/video\/2018-10-31_1540956225.mp4", 
            "http:\/\/leleimg.yewanhuyu.com\/video\/2018-10-26_1540543763.mp4", 
            "http:\/\/leleimg.yewanhuyu.com\/video\/2018-10-19_1539929523.mp4",
            ...
            ]
      
    },
    "desc": ""
}
```
