## 哈哈

# **1. CSS的复合选择器**

## 1.1 什么是复合选择器

在 CSS 中，可以根据选择器的类型把选择器分为`基础选择器`和`复合选择器`，复合选择器是建立在基础选择器之上，对
基本选择器进行组合形成的

- 复合选择器可以更准确、更高效的选择目标元素（标签）
- 复合选择器是由两个或多个基础选择器，通过不同的方式组合而成的
- 常用的复合选择器包括：后代选择器、子选择器、并集选择器、伪类选择器等等

## 1.2 后代选择器

`后代选择器`又称为`包含选择器`，可以选择父元素里面子元素。其写法就是把外层标签写在前面，内层标签写在
后面，中间用空格分隔。当标签发生嵌套时，内层标签就成为外层标签的后代

#### 语法：

```css
元素1 元素2 { 样式声明 }
```

上述语法表示`选择元素 1 里面的所有元素 2` (后代元素)

**例如：**

```css
ul li { 样式声明 } /* 选择 ul 里面所有的 li标签元素 */
```

- 元素1 和 元素2 中间用`空格隔开`
- 元素1 是父级，元素2是子级，最终选择的是`元素2`
- 元素2 可以是儿子，也可以是孙子等，只要是元素1 的后代即可
- 元素1 和 元素2 可以是任意基础选择器

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=98&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对后代选择器的讲解

## 1.3 子选择器

`子元素选择器（子选择器）`只能选择作为某元素的最近一级子元素。简单理解就是选亲儿子元素

#### 语法：

```css
元素1 > 元素2 { 样式声明 }
```

上述语法表示`选择元素1 里面的所有直接后代(子元素) 元素2`

**例如：**

```css
div > p { 样式声明 } /* 选择 div 里面所有最近一级 p 标签元素 */
```

- 元素1 和 元素2 中间用 大于号 隔开
- 元素1 是父级，元素2 是子级，最终选择的是元素2
- 元素2 必须是亲儿子，其孙子、重孙之类都不归他管. 你也可以叫他 亲儿子选择器

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=99&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对子选择器的讲解

## 1.4 并集选择器

`并集选择器可以选择多组标签, 同时为他们定义相同的样式`。通常用于集体声明

`并集选择器`是各选择器`通过英文逗号（,）连接而成`，任何形式的选择器都可以作为并集选择器的一部分

#### 语法：

```css
元素1,
元素2 { 样式声明 }
```

上述语法表示`选择元素1 和 元素2`

**例如：**

```css
 /* 选择 ul 和 div标签元素 */
ul,
div { 样式声明 }
```

- 元素1 和 元素2 中间用`逗号隔开`
- 逗号可以理解为`和`的意思
- 并集选择器通常用于集体声明

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=101&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对并集选择器的讲解

## 1.5 伪类选择器

`伪类选择器`用于向某些选择器添加特殊的效果，比如给链接添加特殊效果，或选择第1个，第n个元素

伪类选择器书写最大的特点是`用冒号（:）表示`，比如 :hover 、 :first-child

因为伪类选择器很多，比如有链接伪类、结构伪类等，所以这里先给大家讲解常用的链接伪类选择器

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=102&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对伪类选择器的讲解

## 1.6 链接伪类选择器

```css
a:link      /* 选择所有未被访问的链接 */
a:visited   /* 选择所有已被访问的链接 */
a:hover     /* 选择鼠标指针位于其上的链接 */
a:active    /* 选择活动链接(鼠标按下未弹起的链接) */
```

一. 链接伪类选择器注意事项

二. 链接伪类选择器实际开发中的写法

!> 链接伪类选择器注意事项：<br>1. 为了确保生效，请按照 `LVHA` 的循顺序声明 :link－:visited－:hover－:active<br>2. 记忆法：love hate 或者 lv 包包 hao<br>3. 因为 a 链接在浏览器中具有默认样式，所以我们实际工作中都需要给链接单独指定样式

#### 链接伪类选择器实际工作开发中的写法：

```css
/* a 是标签选择器 所有的链接 */ 
 a { 
    color: gray;
 }
 /* :hover 是链接伪类选择器 鼠标经过 */
 a:hover { 
    color: red; /* 鼠标经过的时候，由原来的 灰色 变成了红色 */
 }
```

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=102&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=99.2)可以观看pink老师对链接伪类选择器的讲解

## 1.7 :focus 伪类选择器

`:focus伪类选择器`用于选取获得焦点的表单元素。

焦点就是光标，一般情况 `<input>` 类表单元素才能获取，因此这个选择器也主要针对于表单元素来说

#### 语法：

```css
input:focus { 
    background-color:yellow;
}
```

## 1.8 复合选择器总结

<img src="./images/YanCchen_2022-08-22_13-15-41.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=105&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对复合选择器总结的讲解

# **2. CSS的元素显示模式**

了解元素的显示模式可以更好的让我们布局页面
1. 什么是元素的显示模式
2. 元素显示模式的分类
3. 元素显示模式的转换

## 2.1 什么是元素显示模式


<img src="./images/YanCchen_2022-08-22_13-22-46.png" class="img" height="300"/>

世界上离不开男人女人,根据不同特点,通力合作共建美好家园

作用：网页的标签非常多，在不同地方会用到不同类型的标签，了解他们的特点`可以更好的布局我们的网页`

元素显示模式就是`元素（标签）以什么方式进行显示`，比如`<div>`自己占一行，比如一行可以放多个`<span>`

HTML 元素一般分为`块元`素和`行内元`素两种类型

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=106&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对什么是元素显示模式的讲解

## 2.2 块元素和行内元素

### 块元素

常见的块元素有&lt;h1&gt;~&lt;h6&gt;、&lt;p&gt;、&lt;div&gt;、&lt;ul&gt;、&lt;ol&gt;、&lt;li&gt;等，其中 `<div>`标签是`最典型的块元素`

块级元素的特点：<br>
① 比较霸道，自己独占一行<br>
② 高度，宽度、外边距以及内边距都可以控制<br>
③ 宽度默认是容器（父级宽度）的100%<br>
④ 是一个容器及盒子，里面可以放行内或者块级元素

!> 注意：<br>
&raquo; 文字类的元素内不能使用块级元素<br>
&raquo; &lt;p&gt; 标签主要用于存放文字，因此 &lt;p&gt; 里面不能放块级元素，特别是不能放&lt;div&gt;<br>
&raquo; 同理， &lt;h1&gt;~&lt;h6&gt;等都是文字类块级标签，里面也不能放其他块级元素


> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=107&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=23.8)可以观看pink老师对块元素的讲解

### 行内元素

常见的行内元素有 &lt;a>、&lt;strong>、&lt;b>、&lt;em>、&lt;i>、&lt;del>、&lt;s>、&lt;ins>、&lt;u>、&lt;span>等，其中`<span>` 标签是`最典型的行内元素`。有的地方也将行内元素称为`内联元素`

行内元素的特点：<br>
① 相邻行内元素在一行上，一行可以显示多个<br>
② 高、宽直接设置是无效的<br>
③ 默认宽度就是它本身内容的宽度<br>
④ 行内元素只能容纳文本或其他行内元素

!> 注意：<br>
&raquo; 链接里面不能再放链接<br>
&raquo; 特殊情况链接 &lt;a> 里面可以放块级元素，但是给 &lt;a> 转换一下块级模式最安全

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=108&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对行内元素的讲解

## 2.3 行内块元素

在行内元素中有几个特殊的标签 —— &lt;img />、&lt;input />、&lt;td>，它们`同时具有块元素和行内元素的特点`

有些资料称它们为`行内块元素`

行内块元素的特点：<br>
① 和相邻行内元素（行内块）在一行上，但是他们之间会有空白缝隙。一行可以显示多个（行内元素特点）<br>
② 默认宽度就是它本身内容的宽度（行内元素特点）<br>
③ 高度，行高、外边距以及内边距都可以控制（块级元素特点）


> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=109&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对行内块元素的讲解

## 2.4 元素显示模式总结

<img src="./images/YanCchen_2022-08-22_14-07-22.png" class="img"/>

学习元素显示模式的主要目的就是分清它们各自的特点，当我们网页布局的时候，在合适的地方用合适的标签元素

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=110&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对元素显示模式总结的讲解

## 2.5 元素显示模式转换

特殊情况下，我们需要元素模式的转换，简单理解: 一个模式的元素需要另外一种模式的特性

比如想要增加链接 `<a>` 的触发范围

- `转换为块元素：display:block;`
- 转换为行内元素：display:inline;
- `转换为行内块：display: inline-block;`

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=111&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t)可以观看pink老师对元素显示模式转换的讲解

## 2.6 一个小工具的使用 snipaste

[Snipaste](https://zh.snipaste.com/)是一个简单但强大的截图工具，也可以让你将截图贴回到屏幕上

> 常用快捷方式:
> 1. F1 可以截图. 同时测量大小, 设置箭头 书写文字等
> 2. F3 在桌面置顶显示
> 3. 点击图片, alt 可以取色 (按下shift 可以切换取色模式)
> 4. 按下esc 取消图片显示

## 2.7 单行文字垂直居中的代码

?> 这是一个小技巧 

CSS 没有给我们提供文字垂直居中的代码. 这里我们可以使用一个小技巧来实现

解决方案: `让文字的行高等于盒子的高度` 就可以让文字在当前盒子内垂直居中

下面假设我们a的盒子高度设置的40px,我们把文字的行高也设置40px就可以实现文字垂直居中效果

如：

```css
a {
    display: block;         /* 转换为块元素 */
    width: 230px;
    height: 40px;           /* 盒子高度 */
    background-color: #55585a;
    font-size: 14px;
    color: #fff;
    text-decoration: none;
    text-indent: 2em;
    line-height: 40px;      /* 文字行高 */
}
```

!> 我这里假设的a标签是已经转换为块元素了的，不然内元素设置不了宽高

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=114&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=19.0)可以观看pink老师对这个小技巧的讲解

## 2.8 单行文字垂直居中的原理

<img src="./images/YanCchen_2022-08-22_14-58-14.png" class="img"/>

?> **简单理解: 行高的上空隙和下空隙把文字挤到中间了. 是如果行高小于盒子高度,文字会偏上,如果行高大于盒子高度,则文字偏下**

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=114&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=135.1)可以观看pink老师对单行文字垂直居中原理的讲解

# **3. CSS的背景**

通过 CSS 背景属性，可以给页面元素添加背景样式。

背景属性可以设置**背景颜色**、**背景图片**、**背景平铺**、**背景图片位置**、**背景图像固定**等

## 3.1 背景颜色

`background-color` 属性定义了元素的背景颜色

```css
background-color:颜色值;
```

一般情况下元素背景颜色默认值是 transparent（透明），我们也可以手动指定背景颜色为透明色

```css
background-color:transparent;   /* transparent透明的 */
```

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=115&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=70.8)可以观看pink老师对背景颜色的讲解

## 3.2 背景图片

`background-image` 属性描述了元素的背景图像。实际开发常见于 logo 或者一些装饰性的小图片或者是超大的背景图片, 优点是非常便于控制位置. (精灵图也是一种运用场景)

```css
background-image : none | url(url地址)
```

<img src="./images/YanCchen_2022-08-22_15-15-01.png" class="img"/>

!> 注意：背景图片后面的地址，千万不要忘记加 URL， 同时里面的路径不要加引号

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=116&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对背景图片的讲解

## 3.3 背景平铺

如果需要在 HTML 页面上对背景图像进行平铺，可以使用 `background-repeat` 属性

```css
background-repeat: repeat | no-repeat | repeat-x | repeat-y
```

<img src="./images/YanCchen_2022-08-22_15-22-56.png" class="img"/>

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=117&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对背景平铺的讲解

## 3.4 背景图片位置

利用 `background-position` 属性可以改变图片在背景中的位置

```css
background-position: x y;
```

参数代表的意思是：x 坐标和 y 坐标。 可以使用 `方位名词` 或者 `精确单位`

<img src="./images/YanCchen_2022-08-22_15-30-16.png" class="img"/>

**1. 参数是方位名词**
- 如果指定的两个值都是方位名词，则两个值前后顺序无关，比如 left top 和 top left 效果一致
- 如果只指定了一个方位名词，另一个值省略，则第二个值默认居中对齐

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=118&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对方位名词的讲解

> 一些案例：
> - [背景位置案例一](https://www.bilibili.com/video/BV14J4114768?p=119&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)
> - [背景位置案例一](https://www.bilibili.com/video/BV14J4114768?p=120&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)

**2. 参数是精确单位**
- 如果参数值是精确坐标，那么第一个肯定是 x 坐标，第二个一定是 y 坐标
- 如果只指定一个数值，那该数值一定是 x 坐标，另一个默认垂直居中

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=121&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对精确单位的讲解

**3. 参数是混合单位**
- 如果指定的两个值是精确单位和方位名词混合使用，则第一个值是 x 坐标，第二个值是 y 坐标

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=122&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对混合单位的讲解

## 3.5 背景图像固定（背景附着）

`background-attachment` 属性设置背景图像是否固定或者随着页面的其余部分滚动

background-attachment 后期可以制作视差滚动的效果

```css
background-attachment : scroll | fixed
```

<img src="./images/YanCchen_2022-08-22_15-40-14.png" class="img"/>


> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=123&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对背景图像固定的讲解

## 3.6 背景复合写法

为了简化背景属性的代码，我们可以将这些属性合并简写在同一个属性 `background` 中。从而节约代码量

当使用简写属性时，没有特定的书写顺序,一般习惯约定顺序为：

`background:` `背景颜色` `背景图片地址` `背景平铺` `背景图像滚动` `背景图片位置`

```css
background: transparent url(image.jpg) repeat-y fixed top ;
```

这是实际开发中，更提倡的写法


> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=124&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对背景复合写法的讲解


## 3.7 背景色半透明

CSS3 为我们提供了背景颜色半透明的效果

```css
background: rgba(0, 0, 0, 0.3);
```

- 最后一个参数是 alpha 透明度，取值范围在 0~1之间
- 我们习惯把 0.3 的 0 省略掉，写为 background: rgba(0, 0, 0, .3);
- 注意：背景半透明是指盒子背景半透明，盒子里面的内容不受影响
- CSS3 新增属性，是 IE9+ 版本浏览器才支持的
- 但是现在实际开发,我们不太关注兼容性写法了,可以放心使用

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=125&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对背景色半透明的讲解

## 3.8 背景总结

<img src="./images/YanCchen_2022-08-22_16-24-44.png" class="img"/>

**背景图片:实际开发常见于 logo 或者一些装饰性的小图片或者是超大的背景图片, 优点是非常便于控制位置.**

