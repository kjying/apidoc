### 用户头像信息

##### HTTP Method: GET
##### URL: https://host/app/user/head_image.php

#####  Parameters
名称|格式|描述|必须|默认值
---|---|---|---|---
公共参数||||

##### HTTP Response
```json

{
    code: 200,
    data: {
            result: 1,  //0参数错误，1已登录，并返回用户信息，即msg，2未登录，3该用户已经被删除
            msg: {	
                id: "3",    //id
                head_image_status: "3",    //头像状态 0:未上传头像 1:头像待审核 2:审核不通过 3:审核通过
                head_image: "https://api.iofol.cn/public/upload/head_image/2016-04-28/3-1461826216.png",  //用户头像
                head_image_new: "http://p8x3j9qoc.bkt.clouddn.com/headImg_2018-06-12_images_1000002_1528791721473.jpg",//用户上传的头像
           
      }
    },
    desc: ""
}
```