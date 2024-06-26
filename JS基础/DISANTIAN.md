## ***一、JavaScript 流程控制-循环***

# **1. 循环**

循环目的
- 在实际问题中，有许多具有<hong>规律性的重复操作</hong>，因此在程序中要完成这类操作就需要<hong>重复执行某些语句</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=70&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### JS 中的循环

在Js 中，主要有三种类型的循环语句：
- for 循环
- while 循环
- do...while 循环

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=71&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **2. for 循环**

在程序中，一组被重复执行的语句被称之为<hong>循环体</hong>，能否继续重复执行，取决于循环的<hong>终止条件</hong>。由循环体及循环<br>的终止条件组成的语句，被称之为<hongcu>循环语句</hongcu>

## 2.1 语法结构

for 循环主要用于把某些代码循环若干次，通常跟计数有关系。其语法结构如下：

```js
for(初始化变量; 条件表达式; 操作表达式 ){
    //循环体
}
```

- <hongcu>初始化变量：</hongcu>通常被用于初始化一个计数器，该表达式可以使用 var 关键字声明新的变量，这个变量帮我们来记录次数
- <hongcu>条件表达式：</hongcu>用于确定每一次循环是否能被执行。如果结果是 true 就继续循环，否则退出循环
- <hongcu>操作表达式：</hongcu>每次循环的最后都要执行的表达式。通常被用于更新或者递增计数器变量。当然，递减变量也是可以的

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha/?p=71&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

#### 执行过程：

1. 初始化变量，<hong>初始化操作在整个 for 循环只会执行一次</hong>
2. 执行条件表达式，如果为true，则执行循环体语句，否则退出循环，循环结束
3. 执行操作表达式，此时第一轮结束
4. 第二轮开始，直接去执行条件表达式（不再初始化变量），如果为 true ，则去执行循环体语句，否则退出循环
5. 继续执行操作表达式，第二轮结束
6. 后续跟第二轮一致，直至条件表达式为假，结束整个 for 循环

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=72&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

#### 断点调试：

断点调试是指自己在程序的某一行设置一个断点，调试时，程序运行到这一行就会停住，然后你可以一步一步往下调试，调试过程中可以看各个变量当前的值，出错的话，调试到出错的代码行即显示错误，停下

<hongcu>断点调试可以帮我们观察程序的运行过程</hongcu>

浏览器中按 F12--> sources -->找到需要调试的文件-->在程序的某一行设置断点<br>
Watch: 监视，通过watch可以监视变量的值的变化，非常的常用<br>
F11: 程序单步执行，让程序一行一行的执行，这个时候，观察watch中变量的值的变化

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=73&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 2.2 for 循环重复相同的代码

for循环可以重复相同的代码 ，比如我们要输出10句“媳妇我错了”

```js
//  基本写法
for(var i = 1; i <= 10; i++){
    console.log('媳妇我错了~');
}
// 用户输入次数
var num = prompt('请输入次数:')；
for ( var i = 1 ; i <= num; i++) {
    console.log('媳妇我错了~');
} 
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=74&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 2.3 for 循环重复不相同的代码

for 循环还可以重复不同的代码，这主要是因为使用了计数器 ，计数器在每次循环过程中都会有变化

例如，求输出一个人1到100岁：

```js
//  基本写法
for (var i = 1; i <= 100; i++) {
      console.log('这个人今年' + i + '岁了');
}
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=75&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

```js

// for 里面是可以添加其他语句的 
for (var i = 1; i <= 100; i++) {
 if (i == 1) {
    console.log('这个人今年1岁了， 它出生了');
 } else if (i == 100) {
    console.log('这个人今年100岁了，它死了');
  } else {
       console.log('这个人今年' + i + '岁了');
  }
}
```

## 2.4 for 循环重复某些相同操作

for 循环因为有了计数器的存在，我们还可以重复的执行某些操作，比如做一些算术运算

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=76&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

!> 请观看视频通过案例来了解

# **3. 双重 for 循环**

## 3.1 双重 for 循环概述

很多情况下，单层 for 循环并不能满足我们的需求，比如我们要打印一个 5 行 5 列的图形、打印一个倒<br>
直角三角形等，此时就可以通过循环嵌套来实现

<img src="./images/js/YanCchen_2022-10-02_11-16-19.png" class="img" />

<hongcu>循环嵌套</hongcu>是指<hong>在一个循环语句中再定义一个循环语句的语法结构</hong>，例如在for循环语句中，可以<br>再嵌套一个for 循环，这样的 for 循环语句我们称之为<hong>双重for循环</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=81&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 3.2 双重 for 循环语法

```js
for (外循环的初始; 外循环的条件; 外循环的操作表达式) {
    for (内循环的初始; 内循环的条件; 内循环的操作表达式) {  
       需执行的代码;
   }
}
```

- 内层循环可以看做外层循环的语句
- 内层循环执行的顺序也要遵循 for 循环的执行顺序 
- 外层循环执行一次，内层循环要执行全部次数

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=81&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=65.3)可以观看pink老师的讲解

## 3.3 打印五行五列星星

```js
var star = '';
for (var j = 1; j <= 5; j++) {
    for (var i = 1; i <= 5; i++) {
      star += '☆'
    }
    // 每次满 5个星星 就 加一次换行
    star += '\n'
}
console.log(star);
```

核心： 
1. 内层循环负责一行打印五个星星
2. 外层循环负责打印五行

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=82&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 3.4 打印出九九乘法表

#### 分析：

1. 一共有9行，但是每行的个数不一样，因此需要用到双重 for 循环
1. 外层的 for 循环控制行数 i ，循环9次 ，可以打印 9 行  
1. 内层的 for 循环控制每行公式  j  
1. 核心算法：每一行 <hong>公式的个数</hong>正好和<hong>行数</hong>一致， j <= i;
1. 每行打印完毕，都需要重新换一行 
1. 把公式用 i 和 j 替换

#### 实现代码

```js
var str = '';
for (var i = 1; i <= 9; i++) {
    for (var j = 1; j <= i; j++) {
        str += j + 'x' + i + '=' + i * j + '\t';
    }
    str += '\n';
}
console.log(str);
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=85&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 3.5 for 循环小结

- for 循环可以重复执行某些相同代码
- for 循环可以重复执行些许不同的代码，因为我们有计数器
- for 循环可以重复执行某些操作，比如算术运算符加法操作
- 随着需求增加，双重for循环可以做更多、更好看的效果
- 双重 for 循环，外层循环一次，内层 for 循环全部执行
- for 循环是循环条件和数字直接相关的循环
- 分析要比写代码更重要
- 一些核心算法想不到，但是要学会，分析它执行过程
- 举一反三，自己经常总结，做一些相似的案例

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=86&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **4. while 循环**

while 语句可以在条件表达式为真的前提下，循环执行指定的一段代码，直到表达式不为真时结束循环

while语句的语法结构如下：

```js
while (条件表达式) {
    // 循环体代码 
}
```

#### 执行思路：

1. 先执行条件表达式，如果结果为 true，则执行循环体代码；如果为 false，则退出循环，执行后面代码
1. 执行循环体代码
1. 循环体代码执行完毕后，程序会继续判断执行条件表达式，如条件仍为true，则会继续执行循环体，直到循环条件为 false 时，整个循环过程才会结束

!> <hong>注意：</hong><br>1.使用 while 循环时一定要注意，它必须要有退出条件，否则会成为死循环<br>2.while 循环和 for 循环的不同之处在于 while 循环可以做较为复杂的条件判断，比如判断用户名和密码

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=87&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **5. do while 循环**

do... while 语句其实是 while 语句的一个变体。该循环会先执行一次代码块，然后对条件表达式进行判断，如果条件为真，就会重复执行循环体，否则退出循环

do... while 语句的语法结构如下：

```js
do {
    // 循环体代码 - 条件表达式为 true 时重复执行循环体代码
} while(条件表达式);
```

#### 执行思路：

1. 先执行一次循环体代码 
1. 再执行条件表达式，如果结果为 true，则继续执行循环体代码，如果为 false，则退出循环，继续执行后面代码

!> <hongcu>注意：</hongcu><hong>先再执行循环体，再判断，我们会发现 do…while 循环语句至少会执行一次循环体代码</hong>

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=89&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **循环小结**

- JS 中循环有 for 、while 、 do while 
- 三个循环很多情况下都可以相互替代使用
- 如果是用来计次数，跟数字相关的，三者使用基本相同，但是我们更喜欢用 for
- while 和 do…while 可以做更复杂的判断条件，比 for 循环灵活一些 
- while 和 do…while 执行顺序不一样，while 先判断后执行，do…while 先执行一次，再判断执行
- while 和 do…while 执行次数不一样，do…while 至少会执行一次循环体， 而 while 可能一次也不执行
- 实际工作中，<hong>我们更常用for 循环语句</hong>，它写法更简洁直观

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=91&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **6. continue break**

## 6.1 continue 关键字

<hong>continue 关键字</hong>用于立即<hong>跳出本次循环，继续下一次循环</hong>（本次循环体中 continue 之后的代码就会少执行一次）

例如，吃5个包子，第3个有虫子，就扔掉第3个，继续吃第4个第5个包子，其代码实现如下：

```js
 for (var i = 1; i <= 5; i++) {
     if (i == 3) {
         console.log('这个包子有虫子，扔掉');
         continue; // 跳出本次循环，跳出的是第3次循环 
      }
      console.log('我正在吃第' + i + '个包子呢');
 }
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=92&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 6.2 break 关键字

<hong>break 关键字</hong>用于立即<hong>跳出整个循环</hong>（循环结束）

例如，吃5个包子，吃到第3个发现里面有半个虫子，其余的不吃了，其代码实现如下：

```js
for (var i = 1; i <= 5; i++) {
   if (i == 3) {
       console.log('我靠，有脏东西，不吃了');
       break; // 直接退出整个for 循环，跳到整个for下面的语句
   }
   console.log('我正在吃第' + i + '个包子呢');
 }
```

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=93&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# ***二、JavaScript 命名规范以及语法格式***

> 点击[这里](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=94&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **1. 标识符命名规范**

- 变量、函数的命名必须要有意义
- 变量的名称一般用名词  
- 函数的名称一般用动词  

# **2. 操作符规范**

```js
// 操作符的左右两侧各保留一个空格
for (var i = 1; i <= 5; i++) {
   if (i == 3) {
       break; // 直接退出整个 for 循环，跳到整个for循环下面的语句
   }
   console.log('我正在吃第' + i + '个包子呢');
}
```

# **3. 单行注释规范**

```js
for (var i = 1; i <= 5; i++) {
   if (i == 3) {
       break; // 单行注释前面注意有个空格
   }
   console.log('我正在吃第' + i + '个包子呢');
}
```

# **4. 其他规范**

<img src="./images/js/YanCchen_2022-10-02_13-12-18.png" class="img" />