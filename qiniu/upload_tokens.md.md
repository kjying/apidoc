### 获取七牛云token

##### HTTP Method: GET
##### URL: https://host/app/qiniu/upload_tokens.php


#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||

##### HTTP Response
```json
{
    "code": 200,//200 获取成功  400 获取失败
    "data": {
        "upToken": "AYARqpEzEgwHZGV_l733_rxt3PZ1YSZAltW417mm:CMk7erdaUSFSi0J9NdERJVEsNUU=:eyJzY29wZSI6ImxlbGUiLCJkZWFkbGluZSI6MTUyNzIzNzY4NH0="，
        “host”："http://leleimg.yewanhuyu.com/"//文件上传后，将放在域名为leleimg.yewanhuyu.com(http)下面
 
    },
    "desc": "获取成功"
}
```


##### 七牛云上传文件名称规范
* 命名规则：类型 _日期 _文件类型 _用户id _时间戳.文件后缀
* 例子：headImg_2018-05-25_images_1_1527241883.jpg
* 当前的类别：headImg、banner、chat、earnPhoto、gift、identityImg、paycall_screen、photos、others、identityVideo、report
* 文件类型：images、audio、video
