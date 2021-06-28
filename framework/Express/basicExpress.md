# Express Basics

## 什么是Express

## Express的安装
  * $ npm i express或者npm install express。

## Express文件的基础结构
  * const express = require('express');  -- node.js会导入express。
  * const app = express();  -- 创建express对象app。
  * app.get('...')   --是添加endpoints 。（post,put,patch delete等方法也是一样的）
  * 方法的形参(req, res) => {...}  -- 给endpoint注册handler
  * app.listen(8000); -- 指定Express监听这个端口。

## Express运行原理

