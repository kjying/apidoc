### 闪屏主播头像

##### HTTP Method: get
##### URL: https://host/app/index/flash_screen.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---

##### HTTP Response
```json
{
    "code": 200, //200 获取成功 400 返回错误信息
    "data": {
        "result": 1,//1成功
        "msg": {
            "http://leleimg.yewanhuyu.com/headImg_2019-03-26_images_1583751_1553601367487.jpg?imageView2/2/w/500",
            "http://leleimg.yewanhuyu.com/headImg_2019-03-22_images_2026669_1553223462799.jpg?imageView2/2/w/500",
            "http://leleimg.yewanhuyu.com//headImg_2019-02-27_images_2131109_1551252571353672.jpg?imageView2/2/w/500",
        }          
    }
    "desc": "操作成功"
}