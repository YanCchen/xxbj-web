## ***一、JavaScript 运算符***

# **1. 运算符**

运算符（operator）也被称为<hong>操作符</hong>，是用于实现赋值、比较和执行算数运算等功能的符号

JavaScript中常用的运算符有：
- 算数运算符
- 递增和递减运算符
- 比较运算符
- 逻辑运算符
- 赋值运算符

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=42&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **2. 算数运算符**

## 2.1 算术运算符概述

概念：算术运算使用的符号，用于执行两个变量或值的算术运算

<img src="./images/js/YanCchen_2022-09-19_04-35-14.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=42&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=40.3)可以观看pink老师的讲解

## 2.2 浮点数的精度问题

浮点数值的最高精度是 17 位小数，但在进行算术计算时其精确度远远不如整数

```js
var result = 0.1 + 0.2;    // 结果不是 0.3，而是：0.30000000000000004
console.log(0.07 * 100);   // 结果不是 7，  而是：7.000000000000001
```

!> 所以：<hong>不要直接判断两个浮点数是否相等 ! </hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=42&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=300.4)可以观看pink老师的讲解

## 2.3 表达式和返回值

**表达式**：是由数字、运算符、变量等以能求得数值的有意义排列方法所得的组合

简单理解：是由数字、运算符、变量等组成的式子

<hong>表达式最终都会有一个结果，返回给我们，我们成为返回值</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=43&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 2.4 提问

1. 我们怎么判断 一个数能够被整除呢？<br>
<hong>它的余数是0 就说明这个数能被整除， 这就是 %  取余运算符的主要用途</hong>

2. 请问 1 + 2  *  3 结果是？<br>
<hong>结果是7 ，注意算术运算符优先级的，先乘除，后加减，有小括号先算小括号里面的</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=42&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=451.8)可以观看pink老师的讲解

# **3. 递增和递减运算符**

## 3.1 递增和递减运算符概述

如果需要反复给数字变量添加或减去1，可以使用<hongcu>递增（++）和递减（ -- ）</hongcu>运算符来完成

在 JavaScript 中，递增（++）和递减（ -- ）既可以放在变量前面，也可以放在变量后面<br><hong>放在变量前面</hong>时，我们可以称为<hong>前置递增（递减）运算符</hong>，<br><hong>放在变量后面</hong>时，我们可以称为<hong>后置递增（递减）运算符</hong>

!> <hongcu>注意：递增和递减运算符必须和变量配合使用</hongcu>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=44&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 3.2 递增运算符

### 1. 前置递增运算符

<hong>++num</hong> 前置递增，就是自加1，类似于 num =  num + 1，但是 ++num 写起来更简单

使用口诀：<hong>先自加，后返回值</hong>

```js
var  num = 10;
alert(++num + 10);   // 21
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=44&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=187.5)可以观看pink老师的讲解

### 2. 后置递增运算符

<hong>num++</hong> 后置递增，就是自加1，类似于 num =  num + 1 ，但是 num++ 写起来更简单

使用口诀：<hong>先返回原值，后自加 </hong>

```js
var  num = 10;
alert(10 + num++);  // 20
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=45&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 3.3 前置递增和后置递增小结

- 前置递增和后置递增运算符可以简化代码的编写，让变量的值 + 1  比以前写法更简单
- 单独使用时，运行结果相同
- 与其他代码联用时，执行结果会不同 
- 后置：先原值运算，后自加（先人后己） 
- 前置：先自加，后运算（先已后人）
- 开发时，大多使用后置递增/减，并且代码独占一行，例如：num++; 或者 num--;

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=47&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **4. 比较运算符**

## 4.1 比较运算符概述

概念：比较运算符（关系运算符）是<hong>两个数据进行比较时所使用的运算符</hong>，比较运算后，会<hong>返回一个布尔值</hong>（true / false）作为比较运算的结果

<img src="./images/js/YanCchen_2022-09-19_05-26-46.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=48&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 4.2 等号(=)小结

<img src="./images/js/YanCchen_2022-09-19_05-27-37.png" class="img" />

```js
console.log(18 == '18');
console.log(18 === '18'); 
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=48&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=340.3)可以观看pink老师的讲解

# **5. 逻辑运算符**

## 5.1 逻辑运算符概述

概念：逻辑运算符是用来进行布尔值运算的运算符，其返回值也是布尔值。后面开发中经常用于多个条件的判断

<img src="./images/js/YanCchen_2022-09-19_05-51-28.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=49&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.2 逻辑与&&

两边都是 true才返回 true，否则返回 false

<img src="./images/js/YanCchen_2022-09-19_05-53-18.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=49&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=82.4)可以观看pink老师的讲解

## 5.3 逻辑或 ||

两边都为 false 才返回 false，否则都为true

<img src="./images/js/YanCchen_2022-09-19_05-53-52.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=49&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=200.0)可以观看pink老师的讲解

### 逻辑非 ！

逻辑非（<hong>!</hong>）也叫作<hong>取反符</hong>，用来取一个布尔值相反的值，如 true 的相反值是 false

```js
var isOk = !true;
console.log(isOk);  // false
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=49&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=304.9)可以观看pink老师的讲解

## 5.4 短路运算（逻辑中断）

**短路运算的原理：**当有多个表达式（值）时,左边的表达式值可以确定结果时,就不再继续运算右边的表达式的值;

### 1. 逻辑与

- 语法： <hong>表达式1 && 表达式2</hong>
- 如果第一个表达式的值为真，则返回表达式2
- 如果第一个表达式的值为假，则返回表达式1

```js
console.log( 123 && 456 );        // 456
console.log( 0 && 456 );          // 0
console.log( 123 && 456&& 789 );  // 789
```

?> `0` `''` `null` `undefined` `NaN` 都是假，其余是真

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=51&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 2. 逻辑或

- 语法： <hong>表达式1 || 表达式2</hong>
- 如果第一个表达式的值为真，则返回表达式1
- 如果第一个表达式的值为假，则返回表达式2

```js
console.log( 123 || 456 );         //  123
console.log( 0 ||  456 );          //  456
console.log( 123 || 456 || 789 );  //  123
```

```js
// 逻辑中断很重要 它会影响我们程序运行结果
var num = 0;
console.log(123 || num++); // 因为123为真，返回的是123，则num还是0
console.log(num);   // 0
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=52&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **6. 赋值运算符**

概念：用来把数据赋值给变量的运算符

<img src="./images/js/YanCchen_2022-09-19_06-31-00.png" class="img" />

```js
var age = 10;
age += 5;  // 相当于 age = age + 5;
age -= 5;  // 相当于 age = age - 5;
age *= 10; // 相当于 age = age * 10;
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=53&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **7. 运算符优先级**

<img src="./images/js/YanCchen_2022-09-19_06-35-40.png" class="img" />

- 一元运算符里面的<hong>逻辑非优先级很高</hong>
- 逻辑与比逻辑或优先级高

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=54&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# ***二、 JavaScript流程控制-分支***

# **1. 流程控制**

在一个程序执行的过程中，各条代码的执行顺序对程序的结果是有直接影响的。很多时候我们要通过控制代码的执行顺序来实现我们要完成的功能

简单理解： 流程控制就是来控制我们的代码按照什么结构顺序来执行

流程控制主要有三种结构，分别是<hong>顺序结构</hong>、<hong>分支结构</hong>和<hong>循环结构</hong>，这三种结构代表三种代码执行的顺序

<img src="./images/js/YanCchen_2022-09-22_06-13-04.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=56&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **2. 顺序流程控制**

顺序结构是程序中最简单、最基本的流程控制，它没有特定的语法结构，程序会按照<hong>代码的先后顺序，依次执行</hong>，程序中大多数的代码都是这样执行的

<img src="./images/js/YanCchen_2022-09-22_06-14-24.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=56&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=91.7)可以观看pink老师的讲解

# **3. 分支流程控制 if 语句**

## 3.1 分支结构

由上到下执行代码的过程中，根据不同的条件，执行不同的路径代码（执行代码多选一的过程），从而得到不同的结果

<img src="./images/js/YanCchen_2022-09-22_06-23-56.png" class="img" />

JS 语言提供了两种分支结构语句
- if 语句
- switch 语句

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=57&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 3.2 if 语句

### 1. 语法结构

```js
// 条件成立执行代码，否则什么也不做
if (条件表达式) {
    // 条件成立执行的代码语句
}
```

!> <hong>如果if里面的条件表达式结果为真 true 则执行大括号里面的 执行语句<br>如果if条件表达式结果为假 则不执行大括号里面的语句 则执行if后面的代码</hong>

语句可以理解为一个行为，循环语句和分支语句就是典型的语句。一个程序由很多个语句组成，一般情况下，会分割成一个一个的语句

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=57&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=98.9)可以观看pink老师的讲解

### 2. 执行流程

<img src="./images/js/YanCchen_2022-09-22_06-26-24.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=57&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=357.3)可以观看pink老师的讲解

## 3.3 if else语句（双分支语句）

### 1. 语法结构

```js
// 条件成立  执行 if 里面代码，否则执行else 里面的代码
if (条件表达式) {
    // [如果] 条件成立执行的代码
} else {
    // [否则] 执行的代码
}
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=59&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 2. 执行流程

```js
// if如果 else否则
if (条件表达式) {
    // 执行语句1
} else {
    // 执行语句2
}
```

!> <hong>执行思路如果表达式结果为 真 那么执行语句1 否则 执行语句2 </hong>

<img src="./images/js/YanCchen_2022-09-22_06-44-11.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=59&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=327.4)可以观看pink老师的讲解

## 3.4 if else if 语句(多分支语句)

1. 多分支语句 就是利用多个条件来选择不同的语句执行 得到不同的结果 多选1 的过程
2. if else if 语句是多分支语句

### 1. 语法结构

```js
// 适合于检查多重条件。
if (条件表达式1) {
    语句1；
} else if (条件表达式2)  {
    语句2；
} else if (条件表达式3)  {
   语句3；
 ....
} else {
    // 上述条件都不成立执行此处代码
}
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=61&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 2. 执行流程

<img src="./images/js/YanCchen_2022-09-22_07-17-07.png" class="img" />

> 执行思路
> - 如果条件表达式1 满足就执行 语句1 执行完毕后，退出整个if 分支语句
> - 如果条件表达式1 不满足，则判断条件表达式2 满足的话，执行语句2 以此类推
> - 如果上面的所有条件表达式都不成立，则执行else 里面的语句

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=61&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=402.6)可以观看pink老师的讲解

# **4. 三元表达式**

三元表达式也能做一些简单的条件选择。 有三元运算符组成的式子称为三元表达式

### 1. 语法结构

```js
条件表达式1 ? 表达式2 : 表达式3;
```

### 2. 执行思路

- 如果条件表达式1为 true ，则返回表达式2的<hong>值</hong>，如果条件表达式1为 false，则返回表达式3的<hong>值</hong>
- 简单理解： 就类似于  if  else （双分支） 的简写

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=63&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **5. 分支流程控制 switch 语句**

## 5.1 语法结构

switch 语句也是多分支语句，它用于基于不同的条件来执行不同的代码。当要针对变量设置一系列的特定值的选项时，就可以使用 switch

```js
switch( 表达式 ){ 
    case value1:
        // 表达式 等于 value1 时要执行的代码
        break;
    case value2:
        // 表达式 等于 value2 时要执行的代码
        break;
    default:
        // 表达式 不等于任何一个 value 时要执行的代码
}
```

- switch ：开关 转换  ， case ：小例子   选项
- 关键字 switch 后面<hong>括号内</hong>可以是<hong>表达式</hong>或<hong>值</hong>， 通常是一个<hong>变量</hong>
- 关键字 <hong>case</hong> , 后跟一个选项的表达式或值，<hong>后面跟一个冒号</hong>
- switch 表达式的值会与结构中的 case 的值做比较 
- 如果存在匹配<hong>全等</hong>(===) ，则与该 case 关联的代码块会被执行，并在遇<hong>到 break 时停止</hong>，整个 switch 语句代码执行结束
- 如果所有的 case 的值都和表达式的值不匹配，则执行 default 里的代码

!> <hongcu>注意：</hongcu> <hong>执行case 里面的语句时，如果没有break，则继续执行下一个case里面的语句</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=65&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.2 switch 语句和 if else if 语句的区别

1. 一般情况下，它们两个语句可以相互替换
2. switch...case 语句通常处理 case为比较确定值的情况， 而 if…else…语句更加灵活，常用于范围判断(大于、等于某个范围)
3. switch 语句进行条件判断后直接执行到程序的条件语句，效率更高。而if…else 语句有几种条件，就得判断多少次
4. 当分支比较少时，if… else语句的执行效率比 switch语句高
5. 当分支比较多时，switch语句的执行效率比较高，而且结构更清晰

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=68&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解
