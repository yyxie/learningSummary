# 面试js部分


## 1. script defer和 async

	<script defer>: 异步加载，元素解析完成后执行
 	<script async>: 异步加载，但执行时会阻塞元素渲染
async和defer的最主要的区别就是async是异步下载并立即执行，然后文档继续解析，defer是异步加载后解析文档，然后再执行脚本；
它们的核心功能就是异步，那么两种属性怎么去区分什么情况下用哪个那，主要的参考是如果脚本不依赖于任何脚本，并不被任何脚本依赖，那么则使用 defer，如果脚本是模块化的，不依赖于任何脚本，那么则使用 async

## 2. this
在一个函数上下文中，this由调用者提供，由调用函数的方式来决定。如果调用者函数，被某一个对象所拥有，那么该函数在调用时，内部的this指向该对象。如果函数独立调用，那么该函数内部的this，则指向undefined。但是在非严格模式中，当this指向undefined时，它会被自动指向全局对象。在严格模式中,this就指向undefined

## 3. 闭包
闭包的形成需要两个条件。
  ● 在函数内部创建新的函数；
  ● 新的函数在执行时，访问了函数的变量对象；
在google中如果B调用A中的变量则A为闭包

## 4.浅拷贝和深拷贝
● 深拷贝:
	
	多层
	1.json.parse(json.stringify()) 
	* 如果obj里面有时间对象，则JSON.stringify后再JSON.parse的结果，时间将只是字符串的形式。而不是时间对象；
	* 如果obj里有RegExp、Error对象，则序列化的结果将只得到空对象；
	* 如果obj里有函数，undefined，则序列化的结果会把函数或 undefined丢失；
	* 如果obj里有NaN、Infinity和-Infinity，则序列化的结果会变成null
	* JSON.stringify()只能序列化对象的可枚举的自有属性，例如 如果obj中的对象是有构造函数生成的，  则使用JSON.parse(JSON.stringify(obj))深拷贝后，会丢弃对象的constructor；
	*如果对象中存在循环引用的情况也无法正确实现深拷贝；

2. for循环进行拷贝 
   浅拷贝: 值拷贝
		一层for循环
		 var b = {...a};
		var b = Object.assign({},a);
   
## 5.js事件处理顺序

js事件循环规律可大致总结如下:
1.js中有三个任务队列: 主任务队列,job queue, message queue
2.他们的优先级是: 主任务队列 > job queue > message queue
3.每当执行下一个主任务前(或者一个任务完成后), js会根据优先级询问各个任务队列是否为空, 一旦遇到非空任务队列则取其第一个任务执行
https://github.com/Advanced-Frontend/Daily-Interview-Question/issues/7
https://segmentfault.com/a/1190000016923185
附上我的理解
https://www.processon.com/diagraming/5c6e7003e4b07fada4ee8aac


