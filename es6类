## 使用es6 class
- 使用传统的方式构建类

```js
function fun(x,y){
	this.x = x;
	this.y = y
}
fun.prototype.toString = function(){
	return `(${this.x},${this.y})`
}
var f = new fun(1,2);
f.toString();
// 执行结果: "(1,2)"
```

- es6的方式

```js
class fun {
	constructor(x,y){
		this.x = x;
		this.y = y;
	}
	toString(){
		return `(${this.x},${this.y})`
	}
}
const f = new fun(1,2);
f.toString();
// 执行结果"(1,2)"

```
- es6类中关于静态方法,静态变量

```js
// 添加静态变量
fun.staticVar = '1'
// 添加静态方法
fun.staticFun = function(){}
//定义的时候添加静态属性
class A {
    static staticVar = 1;
    static staticFun(){
        console.log('静态方法')
    }
}
```
- es6类中非静态方法,变量

```js
// 定义类的时候就添加的属性
class B {
    x = 1
    fun(){
        console.log(this.x)
    }
}
const b = new B();
// 在实例的时候添加属性
b.y = 1;
b.fun2 = function(){
    console.log(this.y)
}
```
- es类中静态方法，变量和非静态方法，变量之间互相使用
* 类相当于实例的原型，所有在类中定义的方法，都会被实例继承。
* 如果在一个方法前，加上static关键字，就表示该方法不会被实例继承，而是直接通过类来调用，这就称为“静态方法”
* 静态方法不能访问非静态方法，变量； 静态方法只能通过类来调用

```js
class T {
    static f = 1;
    static fun(){console.log(this.f, this.f1)}
    f1 = 2;
    fun1(){console.log(this.f, this.f1)}
}
const t = new T()
t.fun1();
// 打印结果： undefined 2

class TT {
    static f = 1;
    static fun(){console.log(TT.f, this.f1)}
    f1 = 2;
    fun1(){console.log(TT.f, this.f1)}
}
const tt = new TT()
tt.fun1()
// 打印结果： 1 2
TT.fun()
// 打印结果： 1 undefined
```
## 总结的说其实es6中的类和java类的很多特点都是一样的
