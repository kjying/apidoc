### 通话播放视频

1. session.php接口返回预加载视频地址
```javascript
{
	'code': 200,
	'data': {
        "call": {
            // 其他字段省略
            "preload_video_url": "https://wangsu.huataclub.com/video/2022-03-23_1648029358.mp4",  //预加载地址
            "preload_video_seconds": 30,
        }
    },
	'desc': ''
}
```
2. 群拨通知加播放假视频标识
```javascript
{
    // 其他字段省略
    'content_type': 4,          //已有字段 视频通话请求
	'chat_type': 8,             //已有字段 群发消息
    'display_video': 1,         // 不实际拨号 直接播放视频标识
    'force_reload_video': 0,    // =0时使用session接口返回的预加载视频 =1时使用user_info.video_url(如果不是空的话)
    'user_info': {
        'video_url': "",        //已有字段 视频地址
    }
}
```

3. 播放开始后通知服务端
#### 用户点接听后播放视频 并调用该接口 不用等完成播放再调用 [/app/paycall/call_video.php](../paycall/call_video.md)