### 女主播任务情况

##### HTTP Method: Get
##### URL: https://host/app/mailbox/anchor_task.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
*一旦用户的任务完成  socket将推送一下数据（task_type：0 在线时长 1 视频 2语音）{"event":"anchor_task","client_uid":xxx,"msg"=>array('task_id'=>1,'task_type'=>0,'money'=>8,'title'=>'在线时长'),"desc"=>'获取成功'}
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3非法请求 4该用户未通过实名验证 5今日任务未开启
        "timer": 1,    //是否执行定时器  在原有的条件上面添加这个，用来判断当前时间是否在规定的时间段之内
          msg: [ 
            {
                id: "5",//任务id
                current: "3600",//当前值 秒
                complete: "10800",//完成值 3小时
                money: "10",//完成任务后奖励 10元
                status: "0",//0 开始任务 1 完成任务，等待领取奖励 2 已领取任务，任务结束 3任务未完成 已结束
                title:'在线时长晚上8点起到凌晨1点期间在线累计满3小时，即可获取¥10元'
                sub_title:'01:00:00'，
                type：1,//时间类型
            },
            {
                id: "6",//任务id
                current: "1",
                complete: "5",
                money: "5",
                status: "0"
                title:'视频人数：累计接通视频超过30秒的人数满5人且不重复，即可获取¥5元'
                sub_title:'1/5',
                type：0,//非时间类型
            }
        ],
   },
    desc: ""
}
```