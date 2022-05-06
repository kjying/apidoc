### 女性用户资料认证情况

##### HTTP Method: Get
##### URL: https://host/app/paycall/user_identity.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||
##### HTTP Response
```json
{
    "code": 200,
    "data": {
        "result": 1,    //1成功，2未登录 3非法请求 4 该用户未提交过
          msg:{ 
           ‘real_name’：‘’,//真实姓名
           ‘ID_number’：‘’,//身份证
           ‘ID_photo_1’：‘’,//身份证照片
           ‘ID_photo_2’：‘’,//身份证照片
           ‘ID_photo_3’：‘’,//身份证照片
           ‘alipay_id’：‘’,//支付宝账号
           ‘video_url’：‘’,//小视频
           ‘status’：0, // 0 待审核 1 审核通过 2 审核不通过
           ‘weixin’：‘’,//微信号
           ‘wx_status’：0, // 0 待审核 1 审核通过 2 审核不通过
           ‘phone’：‘’,//手机号
           ‘ph_status’：0, // 0 待审核 1 审核通过 2 审核不通过
           ‘qq’：‘’,//QQ号
           ‘qq_status’：0, // 0 待审核 1 审核通过 2 审核不通过
          },
   },
    desc: ""
}
```