### 动态详细信息


#####  字段
名称|格式|描述
---|---|---
id              | int    | 动态id
uid             | int    | 发布人uid
nickname        | string | 发布人昵称
head_image      | string | 发布人头像
title           | string | 标题
pic_url         | string | 主图链接
count_praise    | int    | 点赞数
count_comment   | int    | 评论数
t_create        | int    | 发布时间utc秒
desc            | string | 描述
pics            | array:[[entity_pic]](entity_pic.md) |图片列表
comments        | array:[[entity_comment]](entity_comment.md) | 评论列表
praised         | int    | (自己) 0:未点赞 1:已点赞