## KittyLover接口

* 只有曾调用过lover_info_update接口的用户才会出现在lover_list返回的用户列表里
* lover_info_update 的 info 为字符串 内容由客户端自行定义和解析

| 名称 | URI | 文档链接 |
| :----- | :----| :----: |
|用户补充信息| /app/kitty/lover_info.php |[doc](lover_info.md)|
|用户补充信息更新| /app/kitty/lover_info_update.php |[doc](lover_info_update.md)|
|用户列表| /app/kitty/lover_list.php |[doc](lover_list.md)|
|关注列表| /app/kitty/follow_list.php |[doc](follow_list.md)|