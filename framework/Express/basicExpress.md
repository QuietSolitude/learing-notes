# Express Basics

## 什么是Express

## Express的安装
  * $ npm i express或者npm install express。

## Express文件的基础结构

```js

    const express = require('express');           //node.js会导入express。
    const app = express();                        //创建express对象app。
    app.get( '...' )                              //是添加endpoints 。（app.post,app.put,app.patch app.delete等方法也是一样的）
    app.get( '...' , (req, res) => {...} )        //( req. res ) => {....} 是给endpoint注册handler,app的其它方法也是这样的。
    app.listen(8000);                             //指定Express监听8000这个端口。

```

## Express运行原理

