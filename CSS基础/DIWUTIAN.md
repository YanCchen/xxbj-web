## 哈哈

# **1. 定位**

## 1.1 为什么需要定位

提问： 以下情况使用标准流或者浮动能实现吗？<br>
<hong>1. 某个元素可以自由的在一个盒子内移动位置，并且压住其他盒子</hong>

<img src="./images/YanCchen_2022-08-26_12-58-04.png" class="img" height="250" />

提问： 以下情况使用标准流或者浮动能实现吗？<br>
<hong>2. 当我们滚动窗口的时候，盒子是固定屏幕某个位置的</hong>

<img src="./images/YanCchen_2022-08-26_13-00-28.png" class="img" height="250" />

以上效果，标准流或浮动都无法快速实现，此时<hong>需要定位来实现</hong>

所以：
1. 浮动可以让多个块级盒子一行没有缝隙排列显示， 经常用于横向排列盒子
2. 定位则是可以让盒子自由的在某个盒子内移动位置或者固定屏幕中某个位置，并且可以压住其他盒子

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=222&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.2 定位组成

<hongcu>定位</hongcu>：将盒子<hong>定</hong>在某一个<hong>位</hong>置，所以<hongcu>定位也是在摆放盒子， 按照定位的方式移动盒子</hongcu>

定位 = 定位模式 + 边偏移

<hong>定位模式</hong>用于指定一个元素在文档中的定位方式。<hong>边偏移</hong>则决定了该元素的最终位置

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=223&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 1. 定位模式

定位模式决定元素的定位方式 ，它通过 CSS 的 <hong>position</hong> 属性来设置，其值可以分为四个：

<img src="./images/YanCchen_2022-08-26_13-10-26.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=223&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=82.9)可以观看pink老师的讲解

### 2. 边偏移

边偏移就是定位的盒子移动到最终位置。有 top、bottom、left 和 right 4 个属性

<img src="./images/YanCchen_2022-08-26_13-11-24.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=223&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=148.7)可以观看pink老师的讲解

## 1.3 静态定位static

静态定位是元素的<hong>默认定位方式，无定位的意思</hong>

#### 语法

```css
选择器 { position: static; }
```

- 静态定位按照标准流特性摆放位置，它没有边偏移
- 静态定位在布局时很少用到

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=224&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.4 相对定位relative

<hongcu>相对定位</hongcu>是元素在移动位置的时候，是相对于它<hong>原来的位置</hong>来说的（自恋型）

#### 语法

```css
选择器 { position: relative; }
```

相对定位的特点：（务必记住）
1. 它是相对于自己原来的位置来移动的（<hong>移动位置的时候参照点是自己原来的位置</hong>）
2. <hong>原来</hong>在标准流的<hong>位置</hong>继续占有，后面的盒子仍然以标准流的方式对待它(<hong>不脱标，继续保留原来位置</hong>)

因此，相对定位并没有脱标。它最典型的应用是给绝对定位当爹的。。。

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=224&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=77.2)可以观看pink老师的讲解

## 1.5 绝对定位absolute

<hongcu>绝对定位</hongcu>是元素在移动位置的时候，是相对于它<hong>祖先元素</hong>来说的（拼爹型）

#### 语法

```css
选择器 { position: absolute; }
```

绝对定位的特点：（务必记住）
1. 如果<hong>没有祖先元素</hong>或者<hong>祖先元素没有定位</hong>，则以浏览器为准定位（Document 文档）
2. 如果祖先元素有定位（相对、绝对、固定定位），则以最近一级的有定位祖先元素为参考点移动位置
3. 绝对定位<hong>不再占有原先的位置</hong> （脱标）

所以绝对定位是脱离标准流的

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=225&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.6 子绝父相的由来

弄清楚这个口诀，就明白了绝对定位和相对定位的使用场景

这个“子绝父相”太重要了，是我们学习定位的口诀，是定位中最常用的一种方式这句话的意思是：<hong>子级是绝对定位的话，父级要用相对定位</hong>

① 子级绝对定位，不会占有位置，可以放到父盒子里面的任何一个地方，不会影响其他的兄弟盒子<br>
② 父盒子需要加定位限制子盒子在父盒子内显示<br>
③ 父盒子布局时，需要占有位置，因此父亲只能是相对定位

这就是子绝父相的由来，所以<hong>相对定位经常用来作为绝对定位的父级</hong>

总结： <hong>因为父级需要占有位置，因此是相对定位， 子盒子不需要占有位置，则是绝对定位</hong>

当然，子绝父相不是永远不变的，如果父元素不需要占有位置，<hong>子绝父绝</hong>也会遇到

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=228&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.7 固定定位fixed

<hongcu>固定定位</hongcu>是元素<hong>固定于浏览器可视区的位置</hong>。主要使用场景： 可以在浏览器页面滚动时元素的位置不会改变

#### 语法

```css
选择器 { position: fixed; }
```

固定定位的特点：（务必记住）
1. 以浏览器的可视窗口为参照点移动元素
- 跟父元素没有任何关系
- 不随滚动条滚动
2. 固定定位<hong>不在占有原先的位置</hong>

固定定位也是脱标的，其实固定定位也可以看做是一种特殊的绝对定位

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=230&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

<hongcu>固定定位小技巧： 固定在版心右侧位置</hongcu>

小算法：
1. 让固定定位的盒子 left: 50%. 走到浏览器可视区（也可以看做版心） 的一半位置。
2. 让固定定位的盒子 margin-left: 版心宽度的一半距离。 多走 版心宽度的一半位置
就可以让固定定位的盒子贴着版心右侧对齐了

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=231&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.8 粘性定位sticky

<hongcu>粘性定位</hongcu>可以被认为是相对定位和固定定位的混合。 Sticky 粘性的

#### 语法

```css
选择器 { position: sticky; top: 10px; }
```

粘性定位的特点：
1. 以浏览器的可视窗口为参照点移动元素（固定定位特点）
2. 粘性定位<hong>占有原先的位置</hong>（相对定位特点）
3. 必须添加 top 、left、right、bottom 其中一个才有效

跟页面滚动搭配使用。 兼容性较差，IE 不支持

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=232&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.9 定位的总结

<img src="./images/YanCchen_2022-08-26_14-32-55.png" class="img" />

1. 一定记住 相对定位、固定定位、绝对定位 两个大的特点： 1. 是否占有位置（脱标否） 2. 以谁为基准点移动位置
2. 学习定位重点学会子绝父相

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=233&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.10 定位叠放次序z-index

在使用定位布局时，可能会出现盒子重叠的情况。此时，可以使用 <hong>z-index</hong> 来控制盒子的前后次序 (z轴)

#### 语法

```css
选择器 { z-index: 1; }
```

- 数值可以是正整数、负整数或 0, 默认是 auto，数值越大，盒子越靠上
- 如果属性值相同，则按照书写顺序，后来居上
- 数字后面不能加单位
- 只有定位的盒子才有 z-index 属性

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=234&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.11 定位的拓展

### 1. 绝对定位的盒子居中

加了绝对定位的盒子不能通过 <hong>margin:0 auto</hong> 水平居中，但是可以通过以下计算方法实现水平和垂直居中<br>
① left: 50%;：让盒子的左侧移动到父级元素的水平中心位置<br>
② margin-left: -100px;：让盒子向左移动自身宽度的一半

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=235&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 2. 定位特殊特性

绝对定位和固定定位也和浮动类似
1. 行内元素添加绝对或者固定定位，可以直接设置高度和宽度
2. 块级元素添加绝对或者固定定位，如果不给宽度或者高度，默认大小是内容的大小

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=236&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 3. 脱标的盒子不会触发外边距塌陷

浮动元素、绝对定位(固定定位）元素的都不会触发外边距合并的问题

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=236&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=146.0)可以观看pink老师的讲解

### 4. 绝对定位（固定定位）会完全压住盒子

浮动元素不同，只会压住它下面标准流的盒子，但是不会压住下面标准流盒子里面的文字（图片）

但是绝对定位（固定定位） 会压住下面标准流所有的内容

浮动之所以不会压住文字，因为浮动产生的目的最初是为了做文字环绕效果的。 文字会围绕浮动元素

<img src="./images/YanCchen_2022-08-26_14-48-21.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=237&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **2. 综合案例**

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=238&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

<img src="./images/YanCchen_2022-08-26_15-06-45.png" class="img" />

<img src="./images/YanCchen_2022-08-26_15-07-17.png" class="img" />

1. 大盒子我们类名为： tb-promo 淘宝广告
2. 里面先放一张图片
3. 左右两个按钮 用链接就好了。 左箭头 prev 右箭头 next 
4. 底侧小圆点ul 继续做。 类名为 promo-nav

# **3. 网页布局总结**

通过盒子模型，清楚知道大部分html标签是一个盒子

通过CSS浮动、定位 可以让每个盒子排列成为网页

一个完整的网页，是标准流、浮动、定位一起完成布局的，每个都有自己的专门用法

1. 标准流<br>
可以让盒子上下排列或者左右排列，<hong>垂直的块级盒子显示就用标准流布局</hong>
2. 浮动<br>
可以让多个块级元素一行显示或者左右对齐盒子，<hong>多个块级盒子水平显示就用浮动布局</hong>
3. 定位<br>
定位最大的特点是有层叠的概念，就是可以让多个盒子前后叠压来显示。<hong>如果元素自由在某个盒子内移动就用定位布局</hong>

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=244&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **4. 元素的显示与隐藏**

类似网站广告，当我们点击关闭就不见了，但是我们重新刷新页面，会重新出现！

本质：<hong>让一个元素在页面中隐藏或者显示出来</hong>

1. display 显示隐藏
2. visibility 显示隐藏
3. overflow 溢出显示隐藏

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=245&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 4.1 display属性

display 属性用于设置一个元素应如何显示
- display: none ；隐藏对象
- display：block ；除了转换为块级元素之外，同时还有显示元素的意思

<hong>display 隐藏元素后，不再占有原来的位置</hong>

后面应用及其广泛，搭配 JS 可以做很多的网页特效

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=245&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=89.0)可以观看pink老师的讲解

## 4.2 visibility可见性

<hong>visibility</hong> 属性用于指定一个元素应可见还是隐藏
- visibility：visible ; 元素可视
- visibility：hidden; 元素隐藏

<hong>visibility 隐藏元素后，继续占有原来的位置</hong>

如果隐藏元素想要原来位置， 就用 visibility：hidden

如果隐藏元素不想要原来位置， 就用 display：none (用处更多 重点）

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=246&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 4.3 overflow溢出

<hong>overflow</hong> 属性指定了如果内容溢出一个元素的框（超过其指定高度及宽度） 时，会发生什么

<img src="./images/YanCchen_2022-08-26_16-12-23.png" class="img" />

一般情况下，我们都不想让溢出的内容显示出来，因为溢出的部分会影响布局

但是如果有定位的盒子， 请慎用overflow:hidden 因为它会隐藏多余的部分

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=247&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 小小总结

1. display 显示隐藏元素 但是不保留位置
2. visibility 显示隐藏元素 但是保留原来的位置
3. overflow 溢出显示隐藏 但是只是对于溢出的部分处理

# 综合案例

<img src="./images/YanCchen_2022-08-26_16-23-40.png" class="img" />

1. 练习元素的显示与隐藏
2. 练习元素的定位

核心原理： 原先半透明的黑色遮罩看不见， 鼠标经过 大盒子，就显示出来

遮罩的盒子不占有位置， 就需要用绝对定位 和 display 配合使用

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=248&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解
