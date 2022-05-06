### 新用户获取脚本信息

##### HTTP Method: Get
##### URL: https://host/app/user/script.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
read_num   | int |接受脚本触发条件中阅读脚本小于该数目|true|
new_login|int||false|0

* 无论是否新用户  登录后10秒左右获取一次  new_login=1

##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "new_login": 0,  //==请求中的new_login参数
        "result": 1,    //1成功，2未登录 3该用户不是男性新用户(判断是否为新用户请查看session.php或者login.php里面的用户信息字段isNewUser) 4发起脚本信息已关闭
          msg: [ 
            {
                uid: "5",//主播id
                nickname: "哈哈",//主播昵称
                head_image: "https://api.iofol.cn/public/upload/head_image/2016-04-28/3-1461826216.png",  //用户头像
                timer: "0",//开启时间
                level："2"//等级
                message：[
                   {
                    id:1 //消息id
                    type:3 //消息类型 0 文字 1 图片 2语音 3问题
                    content:"你觉得我长得怎么样" //消息内容
                    answer_one:"漂亮"//选项1
                    answer_two:"性感"//选项2
                    timer:10 //发送下个消息的时间间隔
                    audio_time:0 //语音时长
                    private_type：0//是否为私密图片 0 不是 1是
                    end_point:0 //是否为段落结束点 0 不是 1是
                   }, {
                    id:2 //消息id
                    type:0 //消息类型 0 文字 1 图片 2语音 3问题
                    content:"123" //消息内容
                    timer:10 //发送下个消息的时间间隔
                    audio_time:0 //语音时长
                    private_type：0//是否为私密图片 0 不是 1是
                    end_point:0 //是否为段落结束点 0 不是 1是
                   },
               ]
            },{
                uid: "6",//主播id
                nickname: "恩施",//主播昵称
                head_image: "https://api.iofol.cn/public/upload/head_image/2016-04-28/3-1461826216.png",  //用户头像
                timer: "10",//开启时间
                level："2"//等级
                message：[
                   {
                    id:3 //消息id
                    type:0 //消息类型 0 文字 1 图片 2语音 3问题
                    content:"哈哈" //消息内容
                    timer:10 //发送下个消息的时间间隔
                    audio_time:0 //语音时长
                    private_type：0//是否为私密图片 0 不是 1是
                    end_point:0 //是否为段落结束点 0 不是 1是
                   }, {
                    id:4 //消息id
                    type:0 //消息类型 0 文字 1 图片 2语音 3问题
                    content:"123" //消息内容
                    timer:10 //发送下个消息的时间间隔
                    audio_time:0 //语音时长
                    private_type：0//是否为私密图片 0 不是 1是
                    end_point:0 //是否为段落结束点 0 不是 1是
                   },
               ]
            },
            
        ],
   },
    desc: ""
}
```