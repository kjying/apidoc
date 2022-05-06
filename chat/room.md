### API列表
Method|URL|名称
---|---|---
POST | [/app/chat/room_verify.php](room_verify.md) |提交主播认证
GET  | [/app/chat/room_verify_info.php](room_verify_info.md) | 主播认证信息
POST | [/app/chat/room_create.php](room_create.md) |创建房间
GET | [/app/chat/room_list.php](room_list.md) |房间列表/搜索
GET | [/app/chat/room_enter.php](room_enter.md) |进入房间
GET | [/app/chat/room_leave.php](room_leave.md) |离开房间
GET | [/app/chat/mi_occupy.php](mi_occupy.md) |上麦
GET | [/app/chat/mi_leave.php](mi_leave.md) |下麦
GET | [/app/chat/mi_invite.php](mi_invite.md) |邀请上麦
GET | [/app/chat/mi_invite_accept.php](mi_invite_accept.md) |接受邀请上麦
GET | [/app/chat/mi_set_status.php](mi_set_status.md) |设置麦位状态
POST | [/app/chat/room_chat.php](room_chat.md) |聊天
GET | [/app/chat/gift_config.php](gift_config.md) |礼物配置
GET | [/app/chat/gift_bag.php](gift_bag.md) |礼物背包
POST | [/app/chat/room_gift.php](room_gift.md) |送礼
POST | [/app/chat/room_update.php](room_update.md) | 语聊房间设置
GET  | [/app/chat/room_config.php](room_config.md) | 语聊房间获取标签列表和主题列表
POST | [/app/chat/room_admin_setting.php](room_admin_setting.md) | 语聊房间管理员设置与取消
GET  | [/app/chat/room_user_list.php](room_user_list.md) | 语聊房间用户列表
GET  | [/app/chat/room_user_info.php](room_user_info.md) | 语聊房间用户信息
GET  | [/app/chat/room_blacklist.php](room_blacklist.md) | 房间黑名单列表
GET  | [/app/chat/room_ranking_list.php](room_ranking_list.md) | 房间榜
POST | [/app/chat/room_user_no_speaking.php](room_user_no_speaking.md) | 语聊房间成员是否禁麦
POST | [/app/chat/room_user_block.php](room_user_block.md) | 语聊房间成员踢出房间与解封
GET  | [/app/chat/chat_follow_list.php](chat_follow_list.md) | 获取好友列表、关注列表、关注房间列表
POST | [/app/chat/chat_follow.php](chat_follow.md) | 关注与取消关注
POST | [/app/chat/chat_face.php](chat_face.md) | 语聊用户发送表情
GET  | [/app/chat/chat_music_list.php](chat_music_list.md) | 语聊房间曲库
POST | [/app/chat/chat_music.php](chat_music.md) | 用户添加歌曲
POST | [/app/chat/chat_send.php](chat_send.md) | 发送消息
GET  | [/app/chat/chat_list.php](chat_list.md) | 消息列表
GET  | [/app/chat/chat_contents.php](chat_contents.md) | 聊天记录列表
GET  | [/app/chat/chat_clear.php](chat_clear.md) | 从聊天记录列表删除
GET  | [/app/chat/chat_ignore_all.php](chat_ignore_all.md) | 聊天记录未读清零
GET  | [/app/chat/chat_check_new.php](chat_check_new.md) | 聊天新消息数
GET  | [/app/chat/chat_user_info.php](chat_user_info.md) | 聊吧个人空间
GET  | [/app/chat/chat_anchor_income.php](chat_anchor_income.md) | 房间主播收益
GET  | [/app/chat/commission_record.php](commission_record.md) | 聊吧佣金记录
GET  | [/app/chat/chat_music_play.php](chat_music_play.md) | 歌曲播放完毕,播放下一首
POST  | [/app/chat/report.php](report.md) | 投诉举报
GET  | [/app/chat/room_info.php](room_info.md) | 获取房间信息


### socket消息

#### msg中可能有以下一个或多个种类的消息
* user_enter: 用户进入
* user_leave: 用户离开
* mi_occupy: 有人上麦 mi_seq:麦序 0-4
* mi_leave: 有人下麦 mi_seq:麦序 0-4
* mi_status: 修改麦位状态
* mi_invite: 邀请上麦
* user_chat: 有人聊天
* user_gift: 有人送礼
* user_block: 用户封禁
* admin_setting: 管理员设置
* room_config: 房间配置
* chat_face: 用户发送表情
* chat_music: 当前播放的歌曲
* room_follow：关注房间
* no_speaking: 禁言设置
* room_close: 关闭房间

```json
{
	"event": "room",
	"msg": {
		"room_id": "1000005",
		"user_enter": {
			"uid": "1000004",
			"nickname": "\u5f90\u548c\u5fd7",
			"head_image": "",
			"level": "1",
			"room_status": 0,
			"count_user": "1",
		},
		"user_leave": {
			"uid": "1000004",
			"nickname": "\u5f90\u548c\u5fd7",
			"head_image": "",
			"level": "1",
			"count_user": "1",
		},
		"mi_occupy": {
			"mi_seq": "0",
			"user": {
				"uid": "1000004",
				"nickname": "\u5f90\u548c\u5fd7",
				"head_image": "",
				"level": "1"
			},
			"room_status":"1"
		},
		"mi_leave": {
			"mi_seq": "0"
		},
		"mi_status": {
			"mi_seq": "0",
			"status": "0",
			"voice_status": "0",
			"setting_user_nickname":"昵称", //操作人昵称
		},
		"mi_invite": {
			"mi_seq": "0",
			"mi_fee": "500",	//金币 0为免费
			"invite_nickname": "nickname", // 邀请人昵称
		},
		"user_chat": {
			"user": {
				"uid": "1000005",
				"nickname": "\u679c\u666f\u6f84",
				"head_image": "http:\/\/leleimg.yewanhuyu.com\/headImg_2019-09-14_images_5525350_1568469135122.jpg",
				"level": "16"
			},
			"chat": {
				"uid": 1000005,
				"room_id": "1000005",
				"content": "test_msg",
				"content_type": "1",
				"ctime": 1569728060,
				"id": "3",
				"danmu": 0, 		//是否弹幕
			}
		},
		"user_gift": {
			"super_effect": 1,   // 0:普通;  1:超级跑道
			"user": {
				"uid": "1000004",
				"nickname": "\u5f90\u548c\u5fd7",
				"head_image": "",
				"level": "1"
			},
			"gift": {
				"send_uid": "1000004",
				"room_id": "1000005",
				"get_uid": "1000005",
				"gift_id": "1",
				"count": "1",
				"repeat": "1",
				"cost": 21,
				"profit": 10,
				"ctime": 1569829191,
				"from": 2,
				"version_code": 1,
				"channel": "test001"
			},
			"to_user": {
				"uid": "1000005",
				"nickname": "\u679c\u666f\u6f84",
				"head_image": "http:\/\/leleimg.yewanhuyu.com\/headImg_2019-09-14_images_5525350_1568469135122.jpg",
				"level": "16"
			},
			"giftInfo": {
				"id": "11",
				"name": "\u9e4a\u6865\u76f8\u4f1a",
				"price": "10",
				"img": "http:\/\/sl.yiyuqipai.com\/public\/upload\/gift\/2018-08-15_5b73a2efb365f.png",
				"status": "0",
				"ctime": "1507533843",
				"effect_url": "http:\/\/leleimg.yewanhuyu.com\/gift\/2018-11-29_1543458548.svga",
				"position": "14",
				"orders": "10",
				"en_name": "Magpie Bridge Meeting"
			}
		},
		"user_block": {
			"blocked_user_info": { // 被封禁人信息
				"uid": "123456",
				"nickname": "nickname",
				"head_image" : "http://1.jpg",
				"sex": "1"
			},
			"block_user_info": { // 封禁人信息
				"uid": "123456",
				"nickname": "nickname",
				"head_image" : "http://1.jpg",
				"sex": "1"
			},
			"block_type": "1", // 封禁类型 1-5分钟 2-24小时 3-30天 4-永久踢出
			"unblock_time": "2019-01-01 01:01", // 解封时间
		},
		"admin_setting": {
			"type" : "1", // 1-成为为管理员 2-被取消管理员身份
			"user": { // 设置人
				"uid": "1000004",
				"nickname": "\u5f90\u548c\u5fd7",
				"head_image": "",
				"level": "1"
				"sex": "1"
			},
			"to_user": { // 被设置人
				"uid": "1000005",
				"nickname": "\u679c\u666f\u6f84",
				"head_image": "http:\/\/leleimg.yewanhuyu.com\/headImg_2019-09-14_images_5525350_1568469135122.jpg",
				"level": "16",
				"sex": "1",
			},
		},
		"room_config": {// 只返回当前修改的配置字段
			"img_face": "http://1.jpg", // 房间头像
			"notice": "测试", // 公告
			"name": "name", // 房间名称
			"label": "标签", // 房间标签
			"theme": "沙漠", // 主题名称
		},
		"chat_face": {
			"uid": "123456", // 用户id
			"mi_seq": "1", // 麦位
			"face_url" : "http://1.jpg", // 对应表情url
		},
		"chat_music": { // 如果房间没有歌曲, 返回-1
			"id": "1", // 歌曲id
			"uid": "12345", // 用户id
			"music_name": "name", // 歌曲名                
			"singer": "name", // 歌手
			"music_url": "http://leleimg.yewanhuyu.com/voicechat/music/Kiss The Rain.mp3", // 歌曲url
		},
		"room_follow": {
			"user": {
				"uid": "1000004",
				"nickname": "\u5f90\u548c\u5fd7",
				"head_image": "",
				"level": "1",
				"sex": "1"
			},
		},
		"no_speaking":{
			"user": { // 设置人
				"uid": 1000004,
				"nickname": "\u5f90\u548c\u5fd7",
				"head_image": "",
				"sex": 1
			},
			"to_user": { // 被设置人
				"uid": 1000005,
				"nickname": "\u679c\u666f\u6f84",
				"head_image": "http:\/\/leleimg.yewanhuyu.com\/headImg_2019-09-14_images_5525350_1568469135122.jpg",
				"sex": 1
			},
		},
		"room_close":{
			"room_id":"123456",
			"status":"1", //0正常 1封禁
			"type":"1" // 1关闭房间 2经纪人已解除
		}
	}
}
```

语聊设置socket,因为是全服推送,所以区别于房间socket消息

```json
{
    "event":"chat_config",
    "chat_config":{ // 语聊设置
        "config_chat_notice":"1" // 聊吧全服公告开关 0关 1开
    }
}
```