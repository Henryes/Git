# AJAX
- readyStale状态
- o：请求未初始化
- 1：服务器连接已建立
- 2：请求已接收
- 3：请求处理中
- 4：请求已完成，且响应已就绪
- status
- 200：ok
- 404：未找到页面
- 1XX：信息响应类，表示接收到请求且继续处理
- 2xx:处理成功响应类，表示动作被成功接收、理解和接受
- 3xx:重定向响应类，为了完成指定的动作，必须接受进一步处理
- 4xx:客户端错误，客户请求包含语法错误或者是不能正确执行
- 5xx:服务端错误，服务器不能正确执行一个正确的请求

# AJAX三步骤
- 运用HTML和CSS实现页面，表达信息
- 运用XMLHttpRequest和web服务器进行数据的异步交换
- 运用JavaScript操作DOM，实现动态局部刷新

# XMLHTTPRequest对象

- var request = new XMLHTTPRequest()
- 兼容IE5，IE6语法语句

var request;

if(window.XMLHTTPRequest) {

request = new XMLHTTPRequest();//剩下的浏览器

} else {

request = new ActiveXObject("Microsoft.XMLHTTP");//IE5,IE6

}

# HTTP的GET请求和POST请求：
GET:

- 一般用于信息的获取（他是默认的HTTP请求的方法，一般用来查询操作）
- 使用URL传递参数（发送的信息对任何人都是可见的）
- 对发送信息的数量有限制，一般在2000个字符。

POST:

- 一般用于修改服务器上的资源。（数据会被嵌入HTTP的请求体，一般用于增、删、改操作）
- 发送信息的数量无限制。

# XMLHttpRequest发送请求：
两个方法

- open(method,url,async)
- method：规定HTTP发送请求的方式是get还是post,不区分大小写 ，一般来说用大写
- url：请求地址(相对地址或绝对地址)
- async:同步/异步(false/true)，默认是异步也就是true，可以不用填写
- send(string):发送到服务器（该参数可以填或者不填-----get方法不填或填null，post:一般要填）

例如：

> request.open("POST","create.php",true);
request.setRequestHeader("Content-type","application/x-www-form-urlencoded ")
//设置HTTP头信息--一定要写在open()和send()之间
request.send("name=xxxx&set=xxx");

# php
 PHP代码：

- PHP脚本以<?php 开头 以?>结尾
- PHP文件的默认文件扩展名是 .php
- PHP语句以分号结尾（;）
- 全局变量: php 中 以 $_ 开头的变量
- 测试工具：  Progress Telerik Fiddler Web Debugger

# JSON基本概念
- javaScript对象表示法（javaScript object notation）
- json是存储和交换文本信息的语法，类似xml。它使用键值对的方式来组织，易于人们阅读和编写，同时也易于机器解析和生成
- json是独立于语言的，也就是说不管什么语言，都可以解析json，只需要按照json的规则来就行





