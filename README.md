### 部分文档较久未更新  需以代码为准


##### 公共参数
名称|格式|描述|必须|默认值
---|---|---|---|---
uid|int||是|
session_id|string||是|
imei|string|设备号|是|
version_code|string|版本号|是|
channel|string|渠道|是|
from|string|来源|是|
name_type|string|手机型号|是|
app_from|int|0默认，1安卓分包，2ios分包|是|
local_code|int|0默认，1海外|是|
language|int|中文zh-cn、英文en-ww|是|

##### 返回json
```json
{
    "code": 0,
    "data":{}
}
```
* code：200:正确; 400:参数错误; 500:服务器错误

### 小助手socket消息
{"event":"assistant","msg"=>array(0=>array('content'=>'小助手上线了','ctime'=>1354182154,'content_type'=>0)),"desc"=>'获取成功'}

{"event":"assistant_uid","msg"=>array(0=>array('content'=>'恭喜您成为贵族','ctime'=>1354182154,'content_type'=>3)),"desc"=>'获取成功'}【客户端忽略】

* content_type：0 普通消息 1 女主播审核信息 2 语音模板审核信息 3成为贵族 4主播视频审核 5推广获取金币 6主播微信号审核信息 7后台删除帖子信息 8语聊主播审核信息

//未读数达到限制的状态（status：1（达到） 0（未达到））
'{"event":"set_message_status","uid":1000001,"status":1,"session_id":"sdfsdfsdfs21564654"}'

//修改配置
'{"event":"update_session","desc"=>'修改配置'}'

### 语聊API
[语聊api与socket消息](chat/room.md)

### 所有API列表
Method|URL|名称
---|---|---
POST | [/app/earn/add_plan.php](earn/add_plan.md) |添加赚钱方案
POST | [/app/earn/edit_plan.php](earn/edit_plan.md) |修改赚钱方案
GET | [/app/im/user_conn.php](im/user_conn.md) |和用户即时聊天
POST | [/app/im/auto_reply.php](im/auto_reply.md) |查询女主播的聊天托管信息
POST | [/app/im/get_auto_message.php](im/get_auto_message.md) |获取女主播的聊天托管发送消息的内容
GET | [/app/user/session.php](user/session.md) |初始化客户端
GET | [/app/user/my_info.php](user/my_info.md) |获取用户的个人信息
GET | [/app/user/head_image.php](user/head_image.md) |用户头像信息
GET | [/app/user/check_binding.php](user/check_binding.md) |查询用户绑定状态
GET | [/app/user/follow.php](user/follow.md) |关注与取消关注接口
POST | [/app/user/login.php](user/login.md) |用户登录
POST | [/app/user/logout.php](user/logout.md) |用户退出接口
POST | [/app/user/perfectinfo.php](user/perfectinfo.md) |用户完善资料完成注册接口
POST | [/app/user/register.php](user/register.md) |用户快速注册接口
POST | [/app/user/upload.php](user/upload.md) |用户头像上传接口
POST | [/app/user/photos.php](user/photos.md) |相片接口(上传、删除、查看)
GET | [/app/user/script.php](user/script.md) |获取脚本
POST | [/app/user/send_sms.php](user/send_sms.md) |手机发送验证码接口
POST | [/app/user/phone_verify.php](user/phone_verify.md) |用户手机、微信号绑定、Facebook绑定、Google绑定接口
GET | [/app/user/get_phone.php](user/get_phone.md) |易迅云获取手机号
POST | [/app/report/tipoff2.php](report/tipoff2.md) |通话中举报
GET | [/app/index/user_list.php](index/user_list.md) |首页用户列表
GET | [/app/index/ranking.php](index/ranking.md) |排行榜
GET | [/app/index/user_info.php](index/user_info.md) |用户详情
GET | [/app/index/user_gift_list.php](index/user_gift_list.md) |用户收礼列表
GET | [/app/index/User_search.php](index/User_search.md) |用户搜索
GET | [/app/index/greet_list.php](index/greet_list.md) |一键打招呼
GET | [/app/pay/pay_switch.php](pay/pay_switch) |支付方式
GET | [/app/pay/pay_url.php](pay/pay_url) |获取支付链接
GET | [/app/pay/google_result.php](pay/google_result) |google play验证
GET | [/app/pay/exchange.php](pay/exchange) |金币与秀币兑换
POST | [/app/paycall/cash_draw.php](paycall/cash_draw) |提现
GET | [/app/paycall/index.php](paycall/index.md) |视频语音聊天主页面
GET | [/app/paycall/call.php](paycall/call.md) |用户向主播或主播向用户发起视频请求
GET | [/app/paycall/answer.php](paycall/answer.md) |用户向主播或主播向用户接收视频请求
GET | [/app/paycall/match.php](paycall/match.md) |随机匹配
GET | [/app/paycall/launch_alive.php](paycall/launch_alive.md) |发起方轮询（6s一次）
GET | [/app/paycall/answer_alive.php](paycall/answer_alive.md) |接听方轮询（6s一次）
GET | [/app/paycall/hang_up.php](paycall/hang_up.md) |用户或者主播主动挂断通话
GET | [/app/paycall/user_identity_auth.php](paycall/user_identity_auth.md) |女性用户实名认证
GET | [/app/paycall/earning.php](paycall/earning.md) |赚钱页
GET | [/app/paycall/price_switch.php](paycall/price_switch.md) |主播修改视频语音价格
POST | [/app/paycall/upload_audio_greeting.php](paycall/upload_audio_greeting.md) |上传语音打招呼模板
GET | [/app/paycall/call_list.php](paycall/call_list.md) |通话列表
GET | [/app/paycall/free.php](paycall/free.md) |免费试用视频推荐一个女主播
GET | [/app/paycall/call_mass.php](paycall/call_mass.md) |主播群发视频或语音通知
GET | [/app/paycall/user_identity.php](paycall/user_identity.md) |用户资料认证情况
POST | [/app/paycall/upload_screen.php](paycall/upload_screen.md) |(主播端)通话过程中自动截屏上传
POST | [/app/paycall/user_upload_screen.php](paycall/user_upload_screen.md) |(用户端)通话过程中自动截屏上传
GET | [/app/push/action_notify.php](push/action_notify.md) |用户消息推送用户行为通知接口
GET | [/app/qiniu/upload_tokens.php](qiniu/upload_tokens.md) |获取七牛云token
POST | [/app/mailbox/send_file_msg.php](mailbox/send_file_msg.md) |用户发送发送语音、图片[new]
GET | [/app/mailbox/anchor_task.php](mailbox/anchor_task.md) |女主播任务详情
GET | [/app/mailbox/anchor_task_reward.php](mailbox/anchor_task_reward.md) |女主播点击任务奖励
GET | [/app/mailbox/auto_reply_content.php](mailbox/auto_reply_content.md) |女主播设置托管之后主动发消息
GET | [/app/mailbox/user_auto_reply_content.php](mailbox/user_auto_reply_content.md) |v2.4 行为托管
GET | [/app/mailbox/say_hello.php](mailbox/say_hello.md) |男版一键打招呼
GET | [/app/mailbox/video_list.php](mailbox/video_list.md) |视频列表
POST | [/app/mailbox/dian_zan.php](mailbox/dian_zan.md) |视频点赞
POST | [/app/mailbox/video_upload.php](mailbox/video_upload.md) |视频上传
POST | [/app/user/disturb.php](user/disturb.md) |勿扰模式
GET| [/app/mailbox/video_visit.php](mailbox/video_visit.md) |统计视频观看人数
GET| [/app/user/call_mass_reject.php](user/call_mass_reject.md) |修改用户群拨状态
POST | [/app/paycall/user_register_identity.php](paycall/user_register_identity.md) |女性用户注册（v2.0）
GET | [/app/user/timestamp.php](user/timestamp.md) |获取时间戳
GET | [/app/paycall/income_expense.php](paycall/income_expense.md) |收支明细
GET | [/app/paycall/invite_list.php](paycall/invite_list.md) |推广明细
GET | [/app/paycall/send_gift.php](paycall/send_gift.md) | 用户送礼
GET | [/app/index/phone_fare.php](index/phone_fare.md) |签到列表
POST | [/app/index/phone_fare_reward.php](index/phone_fare_reward.md) |领取话费
POST | [/app/index/sign_in.php](index/sign_in.md) |签到
GET | [/app/index/recharge_list.php](index/recharge_list.md) |充值跑马灯列表
GET | [/app/user/backpack.php](user/backpack.md) |背包列表
GET | [/app/user/sign_list.php](user/sign_list.md) |每日签到列表
GET | [/app/user/sign.php](user/sign.md) |每日签到
GET | [/app/user/lottery_list.php](user/lottery_list.md) |抽奖列表
GET | [/app/user/lottery.php](user/lottery.md) |抽奖
GET | [/app/index/video_list.php](index/video_list.md) |首页视频列表（小程序）
GET | [/app/index/dynamic_video_lis.php](index/dynamic_video_list.md) |动态视频列表
POST | [/app/paycall/call_evaluate.php](paycall/call_evaluate.md) |视频后评价主播
GET | [/app/index/get_openid.php](index/get_openid.md) |小程序获取openid
GET | [/app/index/get_phone_number.php](index/get_phone_number.md) |小程序获取手机号码
GET | [/app/index/user_gift_list.php](index/user_gift_list.md) |查看用户收礼列表接口
GET | [/app/index/user_evaluate_list.php](index/user_evaluate_list.md) |查看用户评价
POST | [/app/index/send_message.php](index/send_message.md) |微信小程序发送消息
GET | [/app/index/user_check_weixin.php](index/user_check_weixin.md) |检查用户是否购买过该主播的微信号/手机号/QQ/图片/视频
POST | [/app/paycall/charge.php](paycall/charge.md) |用户消费
GET | [/app/paycall/choose_chat.php](paycall/choose_chat.md) |选聊
POST | [/app/topic/insert_reply.php](topic/insert_reply.md) |回帖
POST | [/app/topic/insert_topic.php](topic/insert_topic.md) |发帖
POST | [/app/topic/report.php](topic/report.md) |举报回帖
POST | [/app/topic/topic_dian_zan.php](topic/topic_dian_zan.md) |帖子/回帖点赞（取消点赞）
GET | [/app/topic/topic_list.php](topic/topic_list.md) |帖子列表
GET | [/app/topic/topic_info.php](topic/topic_info.md) |帖子详情
GET | [/app/topic/my_topic.php](topic/my_topic.md) |我的帖子/回帖
GET | [/app/topic/delete.php](topic/delete.md) |删除帖子/回帖
GET | [/app/index/phone_bill.php](index/phone_bill.md) | 领取话费跑马灯
GET | [/app/index/flash_screen.php](index/flash_screen.md) | 闪屏主播头像
GET | [/app/game/configure.php](game/configure.md) |打地鼠配置
POST | [/app/game/gophers_hit.php](game/gophers_hit.md) |打地鼠
POST | [/app/game/free_gophers_hit.php](game/free_gophers_hit.md) |免费打地鼠
GET | [/app/game/gift_count.php](game/gift_count.md) |获取用户余额
GET | [/app/game/smash_eggs_configure.php](game/smash_eggs_configure.md) |砸金蛋配置
POST | [/app/game/smash_eggs.php](game/smash_eggs.md) |砸金蛋
POST | [/app/user/bank_edit.php](user/bank_edit.md) |添加银行卡信息
GET | [/app/user/country.php](user/country.md) |国家配置
GET | [/app/user/guard_list.php](user/guard_list.md) |守护列表
GET | [/app/user/user_guard.php](user/user_guard.md) |用户守护主播
GET | [/app/user/remarks_update.php](user/remarks_update.md) |主播备注