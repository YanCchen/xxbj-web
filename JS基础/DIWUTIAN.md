## ***一、JavaScript 作用域***

# **1. 作用域**

## 1.1 作用域概述

通常来说，一段程序代码中所用到的名字并不总是有效和可用的，而限定这个名字的<hong>可用性的代码范围</hong>就是这<br>
个名字的<hongcu>作用域</hongcu>。作用域的使用提高了程序逻辑的局部性，增强了程序的可靠性，减少了名字冲突

JavaScript（es6前）中的作用域有两种：
- 全局作用域
- 局部作用域（函数作用域）

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=135&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.2 全局作用域 

作用于所有代码执行的环境(整个 script 标签内部)或者一个独立的 js 文件

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=135&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=151.1)可以观看pink老师的讲解

## 1.3 局部作用域 （函数作用域）

作用于函数内的代码环境，就是局部作用域。 因为跟函数有关系，所以也称为函数作用域

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=135&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=218.1)可以观看pink老师的讲解

## 1.4 JS 没有块级作用域

- 块作用域由 { } 包括。
- 在其他编程语言中（如 java、c#等），在 if 语句、循环语句中创建的变量，仅仅只能在本 if 语句、本循环语句中使用，如下面的Java代码：

```js
if(true){
  int num = 123;
  system.out.print(num);  // 123
}
system.out.print(num);    // 报错
```

Js中没有块级作用域（在ES6之前）

```js
if(true){
  var num = 123;
  console.log(123); //123
}
console.log(123);   //123
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=137&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **2. 变量的作用域**

## 2.1 变量作用域的分类

在JavaScript中，根据作用域的不同，变量可以分为两种：
- 全局变量
- 局部变量

## 2.2 全局变量

在全局作用域下声明的变量叫做<hongcu>全局变量</hongcu>（<hong>在函数外部定义的变量</hong>）
- 全局变量在代码的任何位置都可以使用
- 在全局作用域下 var 声明的变量 是全局变量
- 特殊情况下，在函数内不使用 var 声明的变量也是全局变量（不建议使用）

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=136&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=35.2)可以观看pink老师的讲解

## 2.3 局部变量

在局部作用域下声明的变量叫做<hongcu>局部变量</hongcu>（<hong>在函数内部定义的变量</hong>）
- 局部变量只能在该函数<hongcu>内部</hongcu>使用
- 在函数内部 var 声明的变量是局部变量
- 函数的<hongcu>形参</hongcu>实际上就是局部变量

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=136&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=98.8)可以观看pink老师的讲解

## 2.4 全局变量和局部变量的区别

- 全局变量：在任何一个地方都可以使用，只有在浏览器关闭时才会被销毁，因此比较占内存
- 局部变量：只在函数内部使用，当其所在的代码块被执行时，会被初始化；当代码块运行结束后，就会被销毁，因此更节省内存空间

# **3. 作用域链**

- 只要是代码，就至少有一个作用域
- 写在函数内部的局部作用域
- 如果函数中还有函数，那么在这个作用域中就又可以诞生一个作用域
- 根据在内部函数可以访问外部函数变量的这种机制，用链式查找决定哪些数据能被内部函数访问，就称作作用域链

作用域链：采取<hongcu>就近原则</hongcu>的方式来查找变量最终的值

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=138&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# ***二、JavaScript 预解析***

# **1. 预解析**

JavaScript 代码是由浏览器中的 JavaScript 解析器来执行的。JavaScript 解析器在运行 JavaScript 代码的时候分为两步：预解析和代码执行

- <hong>预解析：</hong>在当前作用域下, JS 代码执行之前，浏览器会默认把带有 var 和 function 声明的变量在内存中进行提前声明或者定义

- <hong>代码执行：</hong> 从上到下执行JS语句

预解析只会发生在通过 var 定义的变量和 function 上。学习预解析能够让我们知道为什么在变量声明之前访问变量的值是 undefined，为什么在函数声明之前就可以调用函数

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=141&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **2. 变量预解析和函数预解析**

## 2.1 变量预解析（变量提升）

预解析也叫做变量、函数提升

<hongcu>变量提升：</hongcu> 变量的声明会被提升到<hong>当前作用域</hong>的最上面，变量的赋值不会提升

## 2.2 函数预解析（函数提升）

<hongcu>函数提升：</hongcu> 函数的声明会被提升到<hong>当前作用域的</hong>最上面，但是不会调用函数

```js
fn();
function fn() {
    console.log('打印');
}
```

# ***三、JavaScript 对象***

# **1. 对象**

## 1.1 什么是对象？

现实生活中：万物皆对象，对象是<hong>一个具体的事物</hong>，看得见摸得着的实物。例如，一本书、一辆汽车、一个人可以是“对象”，一个数据库、一张网页、一个与远程服务器的连接也可以是“对象”

在 JavaScript 中，对象是一组无序的相关属性和方法的集合，所有的事物都是对象，例如字符串、数值、数组、函数等

对象是由<hong>属性</hong>和<hong>方法</hong>组成的
- 属性：事物的<hongcu>特征</hongcu>，在对象中用<hongcu>属性</hongcu>来表示（常用名词）
- 方法：事物的<hongcu>行为</hongcu>，在对象中用<hongcu>方法</hongcu>来表示（常用动词）

<img src="./images/js/YanCchen_2022-10-07_12-20-37.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=144&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.2 为什么需要对象

保存一个值时，可以使用<hongcu>变量</hongcu>，保存多个值（一组值）时，可以使用<hongcu>数组</hongcu>。如果要保存一个人的完整信息呢？

例如，将“张三疯”的个人的信息保存在数组中的方式为：

```js
var arr = ['张三疯', '男', 128,154];
```

JS 中的对象表达结构更清晰，更强大。张三疯的个人信息在对象中的表达结构如下：

```
张三疯.姓名 =  '张三疯';

张三疯.性别 = '男'; 

张三疯.年龄 = 128; 

张三疯.身高 = 154；
```

```js
person.name =  '张三疯';

person.sex = '男'; 

person.age = 128; 

person.height = 154； 
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=144&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=261.1)可以观看pink老师的讲解

# **2. 创建对象的三种方式**

在 JavaScript 中，现阶段我们可以采用三种方式创建对象（object）：
- 利用<hong>字面量</hong>创建对象 
- 利用<hong> new Object </hong>创建对象 
- 利用<hong>构造函数</hong>创建对象 

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=145&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 2.1 利用字面量创建对象

<hongcu>对象字面量：</hongcu>就是花括号 { } 里面包含了表达这个具体事物（对象）的属性和方法
{ } 里面采取<hongcu>键值对</hongcu>的形式表示 
- 键：相当于属性名
- 值：相当于属性值，可以是任意类型的值（数字类型、字符串类型、布尔类型，函数类型等）

方法冒号后面跟的是一个匿名函数

!> 多个属性或者方法中间用英文逗号隔开

```js
var star = {
    name : 'Yan',
    age : 17,
    sex : '男',
    sayHi : function(){
        alert('大家好啊~');
    }
};
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=145&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=31.0)可以观看pink老师的讲解

### 对象的调用

对象里面的属性调用 : <hong>对象.属性名</hong> ，这个小点 . 就理解为“ <hong>的</hong> ”  
对象里面属性的另一种调用方式 : <hong>对象['属性名']</hong>，注意方括号里面的属性<hong>必须加引号</hong>，我们后面会用      
对象里面的方法调用：<hong>对象.方法名()</hong> ，注意这个方法名字后面<hong>一定加括号</hong>

```js
console.log(star.name)     // 调用名字属性
console.log(star['name'])  // 调用名字属性
star.sayHi();              // 调用 sayHi 方法,注意，一定不要忘记带后面的括号
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=145&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=274.2)可以观看pink老师的讲解

## 变量、属性、函数、方法总结

变量：单独声明赋值，单独存在<br>
属性：对象里面的变量称为属性，不需要声明，用来描述该对象的特征<br>
函数：单独存在的，通过“函数名()”的方式就可以调用<br>
方法：对象里面的函数称为方法，方法不需要声明，使用“对象.方法名()”的方式就可以调用，方法用来描述该对象的行为和功能

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=146&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 2.2 利用new Object创建对象

跟前面的  new Array()  原理一致

```js
var andy = new Obect();
andy.name = 'Yan';
andy.age = 17;
andy.sex = '男';
andy.sayHi = function(){
    alert('大家好啊~');
}
```

- Object() ：第一个字母大写   
- new Object() ：需要 new 关键字
- 使用的格式：<hong>对象.属性 =  值;</hong>     

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=147&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 2.3 利用构造函数创建对象

<hongcu>构造函数：</hongcu>是一种特殊的函数，主要用来初始化对象，即为对象成员变量赋初始值，它总与 new 运算符一起使用。我们可以把对象中一些公共的属性和方法抽取出来，然后封装到这个函数里面

在 js 中，使用构造函数要时要注意以下两点：
- 构造函数用于创建某一类对象，其<hong>首字母要大写</hong>
- 构造函数要<hong>和 new 一起使用</hong>才有意义

#### 语法结构：

```js
// 语法结构
function 构造函数名() {
    this.属性 = 值;
    this.方法 = function() {}
}
// 调用方法
new 构造函数名();
```

#### 如：

```js
function Person(name, age, sex) {
     this.name = name;
     this.age = age;
     this.sex = sex;
     this.sayHi = function() {
      alert('我的名字叫：' + this.name + '，年龄：' + this.age + '，性别：' + this.sex);
    }
}
// 调用
var bigbai = new Person('大白', 100, '男');
var smallbai = new Person('小白', 21, '男');
console.log(bigbai.name);
console.log(smallbai.name);
```

!> <hongcu>注意</hongcu><br>
1.构造函数约定<hong>首字母大写</hong><br>
2.函数内的<hong>属性和方法前</hong>面需要添加 <hong>this</hong> ，表示当前对象的属性和方法<br>
3.构造函数中<hong>不需要 return</hong> 返回结果<br>
4.当我们创建对象的时候，<hong>必须用 new</hong> 来调用构造函数

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=149&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 2.4 构造函数和对象

- 构造函数，如 Stars()，抽象了对象的公共部分，封装到了函数里面，它泛指某一大类（class）  
- 创建对象，如 new Stars()，特指某一个，通过 new 关键字创建对象的过程我们也称为对象实例化 

<img src="./images/js/YanCchen_2022-10-07_13-33-40.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=151&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **3. new关键字**

new 在执行时会做四件事情：
1. 在内存中创建一个新的空对象
2. 让 this 指向这个新的对象
3. 执行构造函数里面的代码，给这个新对象添加属性和方法
4. 返回这个新对象（所以构造函数里面不需要return）

<hongcu>New 和构造函数确认了眼神</hongcu>

<hong>1.他们俩生了一个宝宝<br>2.这个宝宝必须是亲生的 this指向<br>3.教孩子读书一肚子墨水<br>4.长大挣钱回报父母</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=152&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **4. 遍历对象属性**

<hong>for...in </hong>语句用于对数组或者对象的属性进行循环操作

其语法如下：

```js
for (变量 in 对象名字) {
    // 在此执行代码
}
```

语法中的变量是自定义的，它需要符合命名规范，通常我们会将这个变量写为 <hong>k</hong> 或者 <hong>key</hong>

```js
for (var k in obj) {
    console.log(k);      // 这里的 k 是属性名
    console.log(obj[k]); // 这里的 obj[k] 是属性值
}
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=153&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **5. 小结**

1. 对象可以让代码结构更清晰
2. 对象复杂数据类型object
3. 本质：对象就是一组无序的相关属性和方法的集合
4. 构造函数泛指某一大类，比如苹果，不管是红色苹果还是绿色苹果，都统称为苹果
5. 对象实例特指一个事物，比如这个苹果
6. for...in 语句用于对对象的属性进行循环操

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=154&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解