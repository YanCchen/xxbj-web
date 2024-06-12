## ***一、JavaScript 数组***

# **1. 数组的概念**

问：之前学习的数据类型，只能存储一个值。如果我们想存储班级中所有学生的姓名，那么该如何存储呢？<br>
答：可以使用数组(Array)。数组可以把一组相关的数据一起存放，并提供方便的访问(获取）方式

问：什么是数组呢？<br>
答：数组是指<hong>一组数据的集合</hong>，其中的每个数据被称作<hong>元素</hong>，在数组中可以<hong>存放任意类型的元素</hong>。数组是一种将<hong>一组数据存储在单个变量名下</hong>的优雅方式

```js
// 普通变量一次只能存储一个值
var  num = 10; 
// 数组一次可以存储多个值
var arr = [1,2,3,4,5];
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=97&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **2. 创建数组**

## 2.1 数组的创建方式

JS 中创建数组有两种方式：

- 利用  new 创建数组  
- <hong>利用数组字面量创建数组</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=97&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=142.8)可以观看pink老师的讲解

## 2.2 利用 new 创建数组 

```js
var 数组名 = new Array() ；
var arr = new Array();   // 创建一个新的空数组
```

- 注意 Array () ，A 要大写

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=97&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=149.2)可以观看pink老师的讲解

## 2.3 利用数组字面量创建数组 

```js
//1. 使用数组字面量方式创建空的数组
var  数组名 = []；
//2. 使用数组字面量方式创建带初始值的数组
var  数组名 = ['小白','小黑','大黄','瑞奇'];
```

- 数组的字面量是方括号 [ ] 
- 声明数组并赋值称为数组的初始化
- 这种字面量方式也是我们以后<hong>最多使用的方式</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=97&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=215.2)可以观看pink老师的讲解

## 2.4 数组元素的类型

数组中可以存放<hong>任意类型</hong>的数据，例如字符串，数字，布尔值等

```js
var arrStus = ['小白',12,true,28.9];
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=97&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=408.5)可以观看pink老师的讲解

# **3. 获取数组元素**

## 3.1 数组的索引

<hongcu>索引 (下标) ：</hongcu>用来访问数组元素的序号（数组下标从 0 开始）

<img src="./images/js/YanCchen_2022-10-06_09-44-52.png" class="img" />

数组可以通过<hongcu>索引</hongcu>来访问、设置、修改对应的数组元素，我们可以通过“<hong>数组名[索引]</hong>”的形式来获取数组中的元素

这里的<hongcu>访问</hongcu>就是获取得到的意思

```js
// 定义数组
var arrStus = [1,2,3];
// 获取数组中的第2个元素
alert(arrStus[1]);
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=98&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **4. 遍历数组**

问：数组中的每一项我们怎么取出来？<br>
答：可以通过“<hong>数组名[索引号]</hong>”的方式一项项的取出来

```js
var arr = ['red','green', 'blue'];
console.log(arr[0]) // red
console.log(arr[1]) // green
console.log(arr[2]) // blue
```

问：怎么把数组里面的元素全部取出来？<br>
<hongcu>规律：</hongcu><br>
从代码中我们可以发现，从数组中取出每一个元素时，代码是重复的，有所不一样的是<hongcu>索引值在递增</hongcu><br>
<hongcu>答案就是 循环</hongcu>

<hongcu>遍历:</hongcu> 就是把数组中的每个元素从头到尾都访问一次（类似我们每天早上学生的点名）<br>
我们可以通过 <hong>for</hong> 循环索引遍历数组中的每一项

```js
var arr = ['red','green', 'blue'];
for(var i = 0; i < arr.length; i++){
    console.log(arrStus[i]);
}
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=99&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 4.1 数组的长度

使用“<hong>数组名.length</hong>”可以访问数组元素的数量（数组长度）

```js
var arrStus = [1,2,3];
alert(arrStus.length);  // 3
```

!> <hongcu>注意：</hongcu><br>
1.此处数组的长度是<hong>数组元素的个数</hong>，不要和数组的<hong>索引号</hong>混淆<br>
2.当我们数组里面的元素个数发生了变化，这个 length 属性跟着一起变化

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=100&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **5. 数组中新增元素**

## 5.1 通过修改 length 长度新增数组元素

- 可以通过修改 length 长度来实现数组扩容的目的
- length 属性是可读写的

```js
var arr = ['red', 'green', 'blue', 'pink'];
arr.length = 7;
console.log(arr);
console.log(arr[4]);
console.log(arr[5]);
console.log(arr[6]);
```

其中索引号是 4，5，6 的空间没有给值，就是声明变量未给值，默认值就是 <hong>undefined</hong>

<img src="./images/js/YanCchen_2022-10-06_10-46-24.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=104&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.2 通过修改数组索引新增数组元素

- 可以通过修改数组索引的方式追加数组元素
- 不能直接给数组名赋值，否则会覆盖掉以前的数据

```js
var arr = ['red', 'green', 'blue', 'pink'];
arr[4] = 'yancchen';
console.log(arr);
```

这种方式也是我们最常用的一种方式

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=104&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=202.8)可以观看pink老师的讲解

# ***二、JavaScript 函数***

# **1. 函数的概念**

在 JS 里面，可能会定义非常多的相同代码或者功能相似的代码，这些代码可能需要大量重复使用<br>
虽然 for循环语句也能实现一些简单的重复操作，但是比较具有局限性，此时我们就可以使用 <hong>JS 中的函数</hong>

<hongcu>函数：</hongcu>就是封装了一段<hong>可被重复调用执行的</hong><hongcu>代码块</hongcu>。通过此代码块可以实现大量代码的重复使用

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=114&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **2. 函数的使用**

函数在使用时分为两步：<hong>声明函数</hong>和<hong>调用函数</hong>

## 2.1 声明函数

```js
// 声明函数
function 函数名() {
    //函数体代码
}
```

- <hong>function</hong> 是声明函数的关键字,<hong>必须小写</hong>
- 由于函数一般是为了实现某个功能才定义的， 所以通常我们将<hong>函数名</hong>命名为<hong>动词</hong>，比如 getSum

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=115&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 2.2 调用函数

```js
// 调用函数
函数名();  // 通过调用函数名来执行函数体代码
```

- 调用的时候千万<hong>不要忘记添加小括号</hong>
- 口诀：函数不调用，自己不执行

!> <hongcu>注意：</hongcu><hong>声明函数本身并不会执行代码，只有调用函数时才会执行函数体代码</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=115&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=156.6)可以观看pink老师的讲解

## 2.3 函数的封装

- 函数的封装是把一个或者多个功能通过<hongcu>函数的方式封装起来</hongcu>，对外只提供一个简单的函数接口
- 简单理解：封装类似于将电脑配件整合组装到机箱中 ( 类似快递打包）  

<img src="./images/js/YanCchen_2022-10-06_13-17-51.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=115&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=248.1)可以观看pink老师的讲解

# **3. 函数的参数**

## 3.1 形参和实参

在<hong>声明函数时</hong>，可以在函数名称后面的小括号中添加一些参数，这些参数被称为<hongcu>形参</hongcu>，<br>
而在<hong>调用该函数时</hong>，同样也需要传递相应的参数，这些参数被称为<hongcu>实参</hongcu>

<img src="./images/js/YanCchen_2022-10-06_13-35-51.png" class="img" />

<hongcu>参数的作用 : </hongcu>在<hongcu>函数内部</hongcu>某些值不能固定，我们可以通过参数在<hongcu>调用函数时传递</hongcu>不同的值进去

```js
// 带参数的函数声明
function 函数名(形参1, 形参2 , 形参3...) { // 可以定义任意多的参数，用逗号分隔
  // 函数体
}
// 带参数的函数调用
函数名(实参1, 实参2, 实参3...); 
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=117&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 3.2 函数参数的传递过程

```js
// 声明函数
function getSum(num1, num2) {
    console.log(num1 + num2);
}
// 调用函数
getSum(1, 3); // 4
getSum(6, 5); // 11
```

1. 调用的时候实参值是传递给形参的
2. 形参简单理解为：<hongcu>不用声明的变量</hongcu>
3. 实参和形参的多个参数之间用逗号（,）分隔

## 3.3 函数形参和实参个数不匹配问题

<img src="./images/js/YanCchen_2022-10-06_13-57-42.png" class="img" />

```js
function sum(num1, num2) {
    console.log(num1 + num2);
}
sum(100, 200);             // 形参和实参个数相等，输出正确结果
sum(100, 400, 500, 700);   // 实参个数多于形参，只取到形参的个数
sum(200);                  // 实参个数少于形参，多的形参定义为undefined，结果为NaN
```

!> <hongcu>注意：</hongcu>在JavaScript中，形参的默认值是<hong>undefined</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=119&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 3.4 小结

- 函数可以带参数也可以不带参数
- 声明函数的时候，函数名括号里面的是形参，形参的默认值为 undefined
- 调用函数的时候，函数名括号里面的是实参
- 多个参数中间用逗号分隔
- 形参的个数可以和实参个数不匹配，但是结果不可预计，我们尽量要匹配

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=119&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=349.4)可以观看pink老师的讲解

# **4. 函数的返回值**

## 4.1 return 语句

有的时候，我们会希望函数将值返回给调用者，此时通过使用 return 语句就可以实现

return 语句的语法格式如下：

```js
// 声明函数
function 函数名（）{
    ...
    return  需要返回的值；
}
// 调用函数
函数名();    // 此时调用函数就可以得到函数体内return 后面的值
```

- 在使用 return 语句时，函数会停止执行，并返回指定的值
- 如果函数没有 return ，返回的值是 undefined

例如，声明了一个sum()函数，该函数的返回值为666，其代码如下：

```js
// 声明函数
function sum（）{
    ...
    return  666；
}
// 调用函数
sum();      // 此时 sum 的值就等于666，因为 return 语句会把自身后面的值返回给调用者 
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=120&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 4.2 return 终止函数

return 语句之后的代码不被执行

```js
function add(num1，num2){
    //函数体
    return num1 + num2; // 注意：return 后的代码不执行
    alert('我不会被执行，因为前面有 return');
}
var resNum = add(21,6); // 调用函数，传入两个实参，并通过 resNum 接收函数返回值
alert(resNum);          // 27
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=123&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 4.3 return 的返回值

<hong>return 只能返回一个值</hong>。如果用逗号隔开多个值，以最后一个为准

```js
function add(num1，num2){
    //函数体
    return num1，num2;
}
var resNum = add(21,6); // 调用函数，传入两个实参，并通过 resNum 接收函数返回值
alert(resNum);          // 6
```

- 如果想返回多个值可以用数组

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=123&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=116.2)可以观看pink老师的讲解

## 4.4 函数没有 return 返回 undefined

函数都是有返回值的
1. 如果有return 则返回 return 后面的值
1. 如果没有return 则返回 undefined

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=124&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 4.5 break ,continue ,return 的区别

- break ：结束当前的循环体（如 for、while）
- continue ：跳出本次循环，继续执行下次循环（如 for、while）
- return ：不仅可以退出循环，还能够返回 return 语句中的值，同时还可以结束当前的函数体内的代码

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=124&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=102.6)可以观看pink老师的讲解

# **5. arguments的使用**

当我们不确定有多少个参数传递的时候，可以用 <hong>arguments</hong> 来获取。在 JavaScript 中，arguments 实际上<br>
它是当前函数的一个<hong>内置对象</hong>。所有函数都内置了一个 arguments 对象，arguments 对象中<hong>存储了传递的所有实参</hong>

<hongcu>arguments展示形式是一个伪数组</hongcu>，因此可以进行遍历。伪数组具有以下特点：
- 具有 length 属性
- 按索引方式储存数据
- 不具有数组的 push , pop 等方法

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=126&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **6. 函数的两种声明方式**

## 6.1 自定义函数方式(命名函数)

利用函数关键字 function 自定义函数方式

```js
// 声明定义方式
function 函数名() {...}
// 调用  
函数名(); 
```

- 因为有名字，所以也被称为<hong>命名函数</hong>
- 调用函数的代码既可以放到声明函数的前面，也可以放在声明函数的后面

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=133&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 6.2  函数表达式方式(匿名函数）

利用函数表达式方式的写法如下： 

```js
// 这是函数表达式写法，匿名函数后面跟分号结束
var 变量名 = function(){...}；
// 调用的方式，函数调用必须写到函数体下面
变量名();
```

- 因为函数没有名字，所以也被称为匿名函数
- 这个fn 里面存储的是一个函数  
- 函数表达式方式原理跟声明变量方式是一致的
- 函数调用的代码必须写到函数体后面

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=133&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=49.8)可以观看pink老师的讲解