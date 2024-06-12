## ***一、JavaScript 内置对象***

# **1. 内置对象**

- JavaScript 中的对象分为3种：自定义对象 、内置对象、 浏览器对象
- 前面两种对象是JS 基础 内容，属于 ECMAScript
- <hong>内置对象</hong>就是指 JS 语言自带的一些对象，这些对象供开发者使用，并提供了一些常用的或是最基本而必要的功能（属性和方法）
- 内置对象最大的优点就是帮助我们快速开发
- JavaScript 提供了多个内置对象：Math、 Date 、Array、String等

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=156&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **2. 查文档**

## 2.1 MDN

学习一个内置对象的使用，只要学会其常用成员的使用即可，我们可以通过查文档学习，可以通过MDN/W3C来查询

Mozilla 开发者网络（MDN）提供了有关开放网络技术（Open Web）的信息，包括 HTML、CSS 和万维网及 HTML5 应用的 API

MDN:https://developer.mozilla.org/zh-CN/

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=157&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 2.2 如何学习对象中的方法

1. 查阅该方法的功能
1. 查看里面参数的意义和类型
1. 查看返回值的意义和类型
1. 通过 demo 进行测试

# **3. Math 对象**

## 3.1 Math 概述

Math 对象不是构造函数，它具有数学常数和函数的属性和方法。跟数学相关的运算（求绝对值，取整、最大值等）可以使用 Math 中的成员

```js
Math.PI		        // 圆周率
Math.floor() 	      // 向下取整
Math.ceil()            // 向上取整
Math.round()           // 四舍五入版 就近取整   注意 -3.5   结果是  -3 
Math.abs()		     // 绝对值
Math.max()/Math.min()  // 求最大和最小值 
```

!> 注意：上面的<hong>方法必须带括号</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=158&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 3.2 随机数方法 random()

random() 方法可以随机返回一个小数，其取值范围是 [0，1)，左闭右开 0 <= x < 1 

得到一个两数之间的随机整数，包括两个数在内

```js
function getRandom(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min; 
}
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=161&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **4. 日期对象**

## 4.1 Date 概述

- Date 对象和 Math 对象不一样，他是一个构造函数，所以我们需要实例化后才能使用
- Date 实例用来处理日期和时间

## 4.2 Date()方法的使用

#### 1.获取当前时间必须实例化

```js
var now = new Date();
console.log(now);
```

#### 2.Date() 构造函数的参数

如果括号里面有时间，就返回参数里面的时间。例如日期格式字符串为‘2019-5-1’，可以写成new Date('2019-5-1')  或者 new Date('2019/5/1')
- <hong>如果Date()不写参数，就返回当前时间</hong>
- <hong>如果Date()里面写参数，就返回括号里面输入的时间 </hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=163&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 4.3 日期格式化

我们想要 2022-3-9  9:9:9 格式的日期，要怎么办？ <br>
需要获取日期指定的部分，所以我们要手动的得到这种格式 

<img src="./images/js/YanCchen_2022-10-08_09-19-31.png" class="img" />

```js
// 格式化日期 年月日 
var date = new Date();
console.log(date.getFullYear()); // 返回当前日期的年  2019
console.log(date.getMonth() + 1); // 月份 返回的月份小1个月   记得月份+1 呦
console.log(date.getDate()); // 返回的是 几号
console.log(date.getDay()); // 3  周一返回的是 1 周六返回的是 6 但是 周日返回的是 0
// 写一个这样格式的日期 年 月 日 星期
var year = date.getFullYear();
var month = date.getMonth() + 1;
var dates = date.getDate();
var arr = ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六'];
var day = date.getDay();
console.log('今天是：' + year + '年' + month + '月' + dates + '日 ' + arr[day]);
```

```js
// 格式化日期 时分秒
var date = new Date();
console.log(date.getHours()); // 时
console.log(date.getMinutes()); // 分
console.log(date.getSeconds()); // 秒
// 要求封装一个函数返回当前的时分秒 格式 09:09:09
function getTimer() {
    var time = new Date();
    var h = time.getHours();
    h = h < 10 ? '0' + h : h;
    var m = time.getMinutes();
    m = m < 10 ? '0' + m : m;
    var s = time.getSeconds();
    s = s < 10 ? '0' + s : s;
    return h + ':' + m + ':' + s;
}
console.log(getTimer());
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=164&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 4.4 获取日期的总的毫秒形式

Date 对象是基于1970年1月1日（世界标准时间）起的毫秒数

[为什么计算机起始时间从1970年开始?](https://www.zhihu.com/question/27005396/answer/34868386)

我们经常利用总的毫秒数来计算时间，因为它更精确

```js
// 获得Date总的毫秒数(时间戳)  不是当前时间的毫秒数 而是距离1970年1月1号过了多少毫秒数
// 1. 通过 valueOf()  getTime()
var date = new Date();
console.log(date.valueOf()); // 就是 我们现在时间 距离1970.1.1 总的毫秒数
console.log(date.getTime());
// 2. 简单的写法 (最常用的写法)
var date1 = +new Date(); // +new Date()  返回的就是总的毫秒数
console.log(date1);
// 3. H5 新增的 获得总的毫秒数
console.log(Date.now());
```

```js
// 实例化Date对象
var now = new Date();
// 1. 用于获取对象的原始值
console.log(date.valueOf())	
console.log(date.getTime())	
// 2. 简单写可以这么做
var now = + new Date();			
// 3. HTML5中提供的方法，有兼容性问题
var now = Date.now();
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=166&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **5. 数组对象**

## 5.1 数组对象的创建

创建数组对象的两种方式
- 字面量方式

```js
// 1. 利用数组字面量
var arr = [1, 2, 3];
console.log(arr[0]);
```

- new Array()

```js
// 2. 利用new Array()
// var arr1 = new Array();  // 创建了一个空的数组
// var arr1 = new Array(2);  // 这个2 表示 数组的长度为 2  里面有2个空的数组元素 
var arr1 = new Array(2, 3); // 等价于 [2,3]  这样写表示 里面有2个数组元素 是 2和3
console.log(arr1);
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=169&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.2 检测是否为数组

- instanceof 运算符，可以判断一个对象是否属于某种类型
- Array.isArray()用于判断一个对象是否为数组，isArray() 是 HTML5 中提供的方法	 

```js
var arr = [1, 23];
var obj = {};
console.log(arr instanceof Array); // true
console.log(obj instanceof Array); // false
console.log(Array.isArray(arr));   // true
console.log(Array.isArray(obj));   // false
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=170&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.3 添加删除数组元素的方法

<img src="./images/js/YanCchen_2022-10-08_10-22-07.png" class="img" />

```js
// 添加删除数组元素方法
// 1. push() 在我们数组的末尾 添加一个或者多个数组元素   push  推
var arr = [1, 2, 3];
// arr.push(4, 'pink');
console.log(arr.push(4, 'Yan'));

console.log(arr);
// (1) push 是可以给数组追加新的元素
// (2) push() 参数直接写 数组元素就可以了
// (3) push完毕之后，返回的结果是 新数组的长度 
// (4) 原数组也会发生变化
// 2. unshift 在我们数组的开头 添加一个或者多个数组元素
console.log(arr.unshift('red', 'purple'));

console.log(arr);
// (1) unshift是可以给数组前面追加新的元素
// (2) unshift() 参数直接写 数组元素就可以了
// (3) unshift完毕之后，返回的结果是 新数组的长度 
// (4) 原数组也会发生变化

// 3. pop() 它可以删除数组的最后一个元素  
console.log(arr.pop());
console.log(arr);
// (1) pop是可以删除数组的最后一个元素 记住一次只能删除一个元素
// (2) pop() 没有参数
// (3) pop完毕之后，返回的结果是 删除的那个元素 
// (4) 原数组也会发生变化
// 4. shift() 它可以删除数组的第一个元素  
console.log(arr.shift());
console.log(arr);
// (1) shift是可以删除数组的第一个元素 记住一次只能删除一个元素
// (2) shift() 没有参数
// (3) shift完毕之后，返回的结果是 删除的那个元素 
// (4) 原数组也会发生变化
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=171&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.4 数组排序

<img src="./images/js/YanCchen_2022-10-08_10-22-42.png" class="img" />

```js
var arr = [1, 64, 9, 6];
arr.sort(function(a, b) {
    return b - a;      // 降a序
    // return a - b;   // 升序
});
console.log(arr);
```

```js
// 1. 翻转数组
var arr = ['Yan', 'red', 'blue'];
arr.reverse();
console.log(arr);

// 2. 数组排序（冒泡排序）
var arr1 = [13, 4, 77, 1, 7];
arr1.sort(function(a, b) {
    //  return a - b; 升序的顺序排列
    return b - a; // 降序的顺序排列
});
console.log(arr1);
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=174&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.5 数组索引方法

<img src="./images/js/YanCchen_2022-10-08_10-23-32.png" class="img" />

```js
// 返回数组元素索引号方法  indexOf(数组元素)  作用就是返回该数组元素的索引号 从前面开始查找
// 它只返回第一个满足条件的索引号 
// 它如果在该数组里面找不到元素，则返回的是 -1  
// var arr = ['red', 'green', 'blue', 'pink', 'blue'];
var arr = ['red', 'green', 'pink'];
console.log(arr.indexOf('blue'));
// 返回数组元素索引号方法  lastIndexOf(数组元素)  作用就是返回该数组元素的索引号 从后面开始查找
var arr = ['red', 'green', 'blue', 'Yan', 'blue'];

console.log(arr.lastIndexOf('blue')); // 4
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=175&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.6 数组转换为字符串

<img src="./images/js/YanCchen_2022-10-08_10-24-06.png" class="img" />

```js
// 1. toString() 将我们的数组转换为字符串
var arr = [1, 2, 3];
console.log(arr.toString()); // 1,2,3
// 2. join(分隔符) 
var arr1 = ['green', 'blue', 'Yan'];
console.log(arr1.join()); // green,blue,Yan
console.log(arr1.join('-')); // green-blue-Yan
console.log(arr1.join('&')); // green&blue&Yan
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=177&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.7 slice() 和 splice()

<img src="./images/js/YanCchen_2022-10-08_10-24-59.png" class="img" />

slice() 和 splice()  目的基本相同，建议重点看下 splice()

# **6. 字符串对象**

## 6.1 基本包装类型

为了方便操作基本数据类型，JavaScript 还提供了三个特殊的引用类型：String、Number和 Boolean

<hongcu>基本包装类型</hongcu>就是把简单数据类型包装成为复杂数据类型，这样基本数据类型就有了属性和方法

```js
// 下面代码有什么问题？
var str = 'andy';
console.log(str.length);
```

按道理基本数据类型是没有属性和方法的，而对象才有属性和方法，但上面代码却可以执行，这是因为 js 会把基本数据类型包装为复杂数据类型，其执行过程如下 ：

```js
// 1. 生成临时变量，把简单类型包装为复杂数据类型
var temp = new String('andy');
// 2. 赋值给我们声明的字符变量
str = temp;
// 3. 销毁临时变量
temp = null;
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=178&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 6.2 字符串的不可变

指的是里面的值不可变，虽然看上去可以改变内容，但其实是地址变了，内存中新开辟了一个内存空间

```js
var str = 'abc';
str = 'hello';
// 当重新给 str 赋值的时候，常量'abc'不会被修改，依然在内存中
// 重新给字符串赋值，会重新在内存中开辟空间，这个特点就是字符串的不可变
// 由于字符串的不可变，在大量拼接字符串的时候会有效率问题
var str = '';
for (var i = 0; i < 100000; i++) {
    str += i;
}
console.log(str); // 这个结果需要花费大量时间来显示，因为需要不断的开辟新的空间
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=179&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 6.3 根据字符返回位置

字符串所有的方法，都不会修改字符串本身(字符串是不可变的)，操作完成会返回一个新的字符串

<img src="./images/js/YanCchen_2022-10-08_11-10-46.png" class="img" />

```js
// 字符串对象  根据字符返回位置  str.indexOf('要查找的字符', [起始的位置])
var str = '改革春风吹满地，春天来了';
console.log(str.indexOf('春'));
console.log(str.indexOf('春', 3)); // 从索引号是 3的位置开始往后查找
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=180&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 6.4 根据位置返回字符

<img src="./images/js/YanCchen_2022-10-08_11-11-35.png" class="img" />

```js
// 1. charAt(index) 根据位置返回字符
var str = 'andy';
console.log(str.charAt(3));
// 遍历所有的字符
for (var i = 0; i < str.length; i++) {
    console.log(str.charAt(i));
}
// 2. charCodeAt(index)  返回相应索引号的字符ASCII值 目的： 判断用户按下了那个键 
console.log(str.charCodeAt(0)); // 97
// 3. str[index] H5 新增的
console.log(str[0]); // a
```

<img src="./images/js/YanCchen_2022-10-08_11-12-18.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=182&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 6.5 字符串操作方法

<img src="./images/js/YanCchen_2022-10-08_11-13-13.png" class="img" />

```js
// 1. concat('字符串1','字符串2'....)
var str = 'andy';
console.log(str.concat('red'));

// 2. substr('截取的起始位置', '截取几个字符');
var str1 = '改革春风吹满地';
console.log(str1.substr(2, 2)); // 第一个2 是索引号的2 从第几个开始  第二个2 是取几个字符
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=185&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 6.6 replace()方法

<hong>replace()</hong> 方法用于在字符串中用一些字符<hong>替换</hong>另一些字符

其使用格式如下：

```js
replace(被替换的字符串， 要替换为的字符串)；
```

```js
// 替换字符 replace('被替换的字符', '替换为的字符')  它只会替换第一个字符
var str = 'andyandy';
console.log(str.replace('a', 'b'));
// 有一个字符串 'abcoefoxyozzopp'  要求把里面所有的 o 替换为 *
var str1 = 'abcoefoxyozzopp';
while (str1.indexOf('o') !== -1) {
    str1 = str1.replace('o', '*');
}
console.log(str1);
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=186&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 6.7 split()方法

<hong>split()</hong>方法用于切分字符串，它可以将字符串切分为数组。在切分完毕之后，返回的是一个新数组

例如下面代码：  

```js
var str = 'a,b,c,d';
console.log(str.split(','));   // 返回的是一个数组 [a, b, c, d]
```

```js
// 字符转换为数组 split('分隔符')    前面我们学过 join 把数组转换为字符串
var str2 = 'red, Yan, blue';
console.log(str2.split(','));
var str3 = 'red&pink&blue';
console.log(str3.split('&'));
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=186&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=205.1)可以观看pink老师的讲解

## 6.8 toUpperCase() 和 toLowerCase()

- toUpperCase() 	//转换大写
- toLowerCase() 	//转换小写

# ***二、JavaScript 简单类型与复杂类型***

# **1. 简单类型与复杂类型**

简单类型又叫做基本数据类型或者<hong>值类型</hong>，复杂类型又叫做<hong>引用类型</hong>

- 值类型：简单数据类型/基本数据类型，在存储时变量中存储的是值本身，因此叫做值类型<br>
string ，number，boolean，undefined，null

- 引用类型：复杂数据类型，在存储时变量中存储的仅仅是地址（引用），因此叫做引用数据类型<br>
通过 new 关键字创建的对象（系统对象、自定义对象），如 Object、Array、Date等

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=188&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **2. 堆和栈**

堆栈空间分配区别：

　　1、栈（操作系统）：由操作系统自动分配释放存放函数的参数值、局部变量的值等。其操作方式类似于数据结构中的栈<br>
<hong>简单数据类型存放到栈里面</hong>

　　2、堆（操作系统）：存储复杂类型(对象)，一般由程序员分配释放，若程序员不释放，由垃圾回收机制回收<br>
<hong>复杂数据类型存放到堆里面</hong>

<img src="./images/js/YanCchen_2022-10-08_11-58-02.png" class="img" />

!> <hongcu>注意：</hongcu><hong>JavaScript中没有堆栈的概念，通过堆栈的方式，可以让大家更容易理解代码的一些执行方式，便于将来学习其他语言</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=188&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=163.2)可以观看pink老师的讲解

# **3. 简单类型的内存分配**

- 值类型（简单数据类型）： string ，number，boolean，undefined，null
- 值类型变量的数据直接存放在变量（栈空间）中

<img src="./images/js/YanCchen_2022-10-08_11-59-49.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=188&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=251.3)可以观看pink老师的讲解

# **4. 复杂类型的内存分配**

- 引用类型（复杂数据类型）：通过 new 关键字创建的对象（系统对象、自定义对象），如 Object、Array、Date等
- 引用类型变量（栈空间）里存放的是地址，真正的对象实例存放在堆空间中

<img src="./images/js/YanCchen_2022-10-08_12-00-34.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=188&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=353.7)可以观看pink老师的讲解

# **5. 简单类型传参**

函数的形参也可以看做是一个变量，当我们把一个值类型变量作为参数传给函数的形参时，其实是把变量在栈空间里的值复制了一份给形参，那么在方法内部对形参做任何修改，都不会影响到的外部变量

```js
function fn(a) {
    a++;
    console.log(a); 
}
var x = 10;
fn(x);
console.log(x)；
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=189&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **6. 复杂类型传参**

函数的形参也可以看做是一个变量，当我们把引用类型变量传给形参时，其实是把变量在栈空间里保存的堆地址复制给了形参，形参和实参其实保存的是同一个堆地址，所以操作的是同一个对象

```js
function Person(name) {
    this.name = name;
}
function f1(x) { // x = p
    console.log(x.name); // 2. 这个输出什么 ? 刘德华
    x.name = "张学友";
    console.log(x.name); // 3. 这个输出什么 ? 张学友
}
var p = new Person("刘德华");
console.log(p.name);    // 1. 这个输出什么 ? 刘德华
f1(p);
console.log(p.name);    // 4. 这个输出什么 ? 张学友
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=190&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解