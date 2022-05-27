# 交互式表演服务端接口说明

### 现有接口改动
1. [api:gifts](/paycall/gifts.md) 增加show类型礼物 show_vip类型礼物
2. api:paycall/call 返回内容增加字段showEnable(0|1), 标识交互式表演功能入口是否开放.
3. api:paycall/answer 返回内容增加字段showEnable(0|1), 标识交互式表演功能入口是否开放.
4. [api:call_evaluate](/paycall/call_evaluate.md) 增加show_rating参数(表演评分)
5. [api:ranking](/index/ranking.md) 增加sub_type=9为表演收入榜

#### 客户端检查本方是否可用交互式表演功能, 双方都可用时显示相关ui

### api
| 名称 | URI | 文档链接 |
| :----- | :----| :----: |
|主播邀请| /app/show/anchor_invite.php |[doc](anchor_invite.md)|
|用户拒绝| /app/show/user_reject.php |[doc](user_reject.md)|
|用户邀请| /app/show/user_invite.php |[doc](user_invite.md)|
|主播接受| /app/show/anchor_accept.php |[doc](anchor_accept.md)|
|主播拒绝| /app/show/anchor_reject.php |[doc](anchor_reject.md)|

### message
名称|格式|描述
---|---|---
uid             | int    | 发送者uid
receive_uid     | int    | 接受人uid
ctime           | int    | utc秒
gid             | int    | 表演礼物id
show_id         | int    | 表演id
chat_type       | int    | 见下面chat_type说明
content_type    | int    | 8 (本字段只是为了兼容其他代码避免报错)
content         | string | 空字符串 (本字段只是为了兼容其他代码避免报错)
gift_data       | object | 见下面gift_data说明

### chat_type
message_type|value|desc
---|---|---
anchor_invite|51|主播邀请用户
user_invite|52|用户邀请主播
anchor_accept|53|主播同意表演
user_accept|54|用户同意送礼观看表演
anchor_reject|55|主播拒绝表演
user_reject|56|用户拒绝送礼
user_balance|57|用户金币不足
user_accept_self|58|用户送礼观看表演(自己邀请)

### gift_data
名称|格式|描述
---|---|---
call_id         | int    | 通话id
show_id         | int    | 表演id
gid             | int    | 表演礼物id
name            | string | 礼物名(表演名)
img             | string | 图标url
num             | int    | 数量 固定值1
effect_url      | string | 特效url
unit_profit     | int    | 主播收益 0 暂未计算
price           | int    | 金币价格


### 交互流程
------
#### 1.主播发起 用户接受
```mermaid
sequenceDiagram
    participant girl
    participant server
    participant user
    girl->>server: api:anchor_invite
    server->>user: message:anchor_invite
    user->>server: api:send_gift
    server->>girl: 成功:message:user_accept
    server-->>girl: 失败:message:user_balance
```




#### 2.主播发起 用户拒绝
```mermaid
sequenceDiagram
    participant girl
    participant server
    participant user
    girl->>server: api:anchor_invite
    server->>user: message:anchor_invite
    user->>server: api:user_reject
    server->>girl: message:user_reject
```

#### 3.用户发起 主播接受
```mermaid
sequenceDiagram
    participant girl
    participant server
    participant user
    user->>server: api:user_invite
    server->>girl: message:user_invite
    girl->>server: api:anchor_accept
    server->>user: message:anchor_accept
    user->>server: api:send_gift
    server->>girl: 成功:message:user_accept_self
    server-->>girl: 失败:message:user_balance
```

#### 4.用户发起 主播拒绝
```mermaid
sequenceDiagram
    participant girl
    participant server
    participant user
    user->>server: api:user_invite
    server->>girl: message:user_invite
    girl->>server: api:anchor_reject
    server->>user: message:anchor_reject
```

#### 数据库
* show full columns from tb_show

#### 管理后台
1. 表演菜单点击统计  主播点击次数/用户点击次数, 即由主播/用户发起的次数 根据tb_show.inviter_type分别统计. 通话次数为tb_pay_call.show_enable=1的次数
2. 主播表演次数流水统计 tb_show.finish_time>0为成功, 金币关联tb_gift表, 评价为tb_show.rating.
