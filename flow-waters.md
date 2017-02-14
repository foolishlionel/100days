### 20170208
- 浏览器对象document，javascript html dom
- javascript URLEncode
	- [encodeURL](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/encodeURI)
	- [encodeURLComponent](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/encodeURIComponent)
	- [stackoverflow](http://stackoverflow.com/questions/4540753/should-i-use-encodeuri-or-encodeuricomponent-for-encoding-urls)
	- [jb51](http://www.jb51.net/article/22880.htm)
- null和undefined
	- [javascript中null, NaN, undefined的区别](http://www.cnblogs.com/qiantuwuliang/archive/2010/01/12/1645302.html) - cnblog
	- [null和undefined区别](http://www.ruanyifeng.com/blog/2014/03/undefined-vs-null.html) - 阮一峰
- ssh-keygen -t rsa ....
- 创建个人博客站点pythonhater.github.io - [finished]

### 20170209
- javascript基本数据类型和对象
	- var myName = String("flion") // 基本类型String
	- var myName = new String("flion") // String对象
- javascript位操作符
	- & 与操作
	- | 或操作
	- ^ 异或操作
	- ~ 非操作
	- << 左移位	
	- >> 右移位	
	- >>> 补零的右移位

### 20170210
- nodejs中的`=>`的作用
- nodejs中的next作用

> 问题由来[github yyss8/scBlog](https://github.com/yyss8/scBlog/)

### 20170212


HTML里面使用CSS的几种方式

#### 1. 直接添加在HTML的标识符(tag)里

```
// <tag style="properties">网页内容</tag>，例如
<p style="font-family:Geneva, Arial, Helvetica, sans-serif;font-size:9px;color:#ff9900">CSS</p>
```

#### 2. 添加在HTML的头信息标识符<head>里

```
<html>
	<head>
		<title>页面标题</title>
		<style>
			h2{
				font-family:幼圆;
				color:red;
			}
		</style>
	</head>
	
	<body>
		<h2>CSS标记</h2>
		<p>CSS标记的正文内容1</p>
	</body>
</html>
```

#### 3. **链接样式表** 同样添加在HTML的头信息标识符里

```
<head>
<link rel="stylesheet" href="main.css" type="text/css">
</head>
```
main.css是单独保存的样式表文件，其中不能包含<style>标识符，并且只能以css为后缀。如果用作一个web站点的话建议使用链接样式表的方式，如果需要修改web站点的页面的话，只需要修改几个css文件就可以使整个web页面更新，缩短了修改时间和提高了工作效率。

#### 4. @import

```
<style type="text/css" media="screen">
	@import "all.css"
<style>
```

link和@import的区别：服务对象不一样，@import为CSS服务，link为当前的页服务，@import会优先执行。



### 20170214
- div和p的区别
[参考链接](http://www.w3school.com.cn/tags/tag_span.asp)
