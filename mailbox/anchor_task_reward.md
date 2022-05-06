### 女主播点击领取任务奖励

##### HTTP Method: Get
##### URL: https://host/app/mailbox/anchor_task_reward.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
task_id|int|任务id|true|
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3非法请求 4该用户未通过实名验证 5 task_id 与 用户id 不一致 6 该任务未完成或已经被领取了 7生成收入流水失败 8任务状态修改失败
   },
    desc: "操作成功"//上面的错误信息
}
```