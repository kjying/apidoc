### 签到列表

##### HTTP Method: GET
##### URL: https://host/app/index/phone_fare.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||

##### HTTP Response
```json
{
    code: 200,
    data: {
       result: 1,//1 获取成功 2 请先登录 3 没有签到数据
       msg: {
            id: "1", //签到id
            uid: "1003597",
            fare: "10", //单位 元
            sign_in: "7", //总共签到的天数
            sign_in_total: 0,//当前连续签到的天数 -1表示断签
            last_sign_time: 1823315444, //最后一次签到的时间
            status: "0", //0 任务未开始 1任务开始 2任务结束未领取奖励 3任务结束领取话费,等待下一轮签到 4任务结束
            phone: null,
            ctime: 1820315444,
            stime: 1853315444,
            is_sign_today: 0, //当天是否已经签到
            day_fare: [0,0,0,0,0,0,10] //每天送钱 单位 元
            current_fare：0//当前任务领取的话费个数 从0开始
            etime：2023315444 //结束时间
            }
    },
    desc: "获取成功"
}