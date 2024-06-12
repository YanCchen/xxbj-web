## **一、CSS的三大特性**

# **1. CSS的三大特性**

CSS 有三个非常重要的三个特性：层叠性、继承性、优先级

## 1.1 层叠性

相同选择器给设置相同的样式，此时一个样式就会`覆盖（层叠）`另一个冲突的样式。层叠性主要解决样式冲突的问题

> 层叠性原则：
> - 样式冲突，遵循的原则是`就近原则`，哪个样式离结构近，就执行哪个样式
> - 样式不冲突，不会层叠

<img src="./images/YanCchen_2022-08-22_19-28-34.png" class="img" height="250" />

CSS层叠性口诀：`长江后浪推前浪，前浪死在沙滩上`

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=129&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对层叠性的讲解

## 1.2 继承性

现实中的继承: 我们继承了父亲的姓

CSS中的继承: 子标签会继承父标签的某些样式，如文本颜色和字号。简单的理解就是：子承父业

<img src="./images/YanCchen_2022-08-22_19-38-01.png" class="img" height="250" />

- 恰当地使用继承可以简化代码，降低 CSS 样式的复杂性
- 子元素可以继承父元素的样式（text-，font-，line-这些元素开头的可以继承，以及color属性）
- 继承性口诀：`龙生龙，凤生凤，老鼠生的孩子会打洞`

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=130&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对继承性的讲解

### 行高的继承性

```css
body {
    font:12px/1.5 Microsoft YaHei；
}
```

- 行高可以跟单位也可以不跟单位
- 如果子元素没有设置行高，则会继承父元素的行高为 1.5
- 此时子元素的行高是：当前子元素的文字大小 * 1.5 
- `body 行高 1.5 这样写法最大的优势就是里面子元素可以根据自己文字大小自动调整行高`

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=131&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对行高继承性的讲解

## 1.3 优先级

当同一个元素指定多个选择器，就会有优先级的产生
- 选择器相同，则执行层叠性
- 选择器不同，则根据`选择器权重`执行

**选择器权重如下表所示:**

<img src="./images/YanCchen_2022-08-22_19-59-21.png" class="img" height="250" />

> 优先级注意点:
> 1. 权重是有4组数字组成,但是不会有进位
> 2. 可以理解为类选择器永远大于元素选择器, id选择器永远大于类选择器,以此类推..
> 3. 等级判断从左向右，如果某一位数值相同，则判断下一位数值
> 4. 可以简单记忆法: 通配符和继承权重为0, 标签选择器为1,类(伪类)选择器为 10, id选择器 100, 行内样式表为1000, !important 无穷大
> 5. `继承的权重是0`， 如果该元素没有直接选中，不管父元素权重多高，子元素得到的权重都是 0

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=132&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对优先级的讲解

`权重叠加：`如果是复合选择器，则会有权重叠加，需要计算权重
- div ul li ------> 0,0,0,3
- .nav ul li ------> 0,0,1,2
- a:hover -----—> 0,0,1,1
- .nav a ------> 0,0,1,1

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=134&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对优先级权重叠加的讲解

> 如果你还是有点懵，你可以通过[这个](https://www.bilibili.com/video/BV14J4114768?p=135&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)练习题讲解视频会更容易明白

# **2. CSS的注释**

注释用于解释代码，它们会被浏览器忽略。CSS 中的注释以“ `/*` ”开头，以“ `*/` ”结尾

```css
/* 需要注释的内容 */
```

# **二、盒子模型**

# **1. 盒子模型**

页面布局要学习三大核心, 盒子模型, 浮动 和 定位. 学习好盒子模型能非常好的帮助我们布局页面

## 1.1 看透网页布局的本质

<img src="./images/YanCchen_2022-08-23_10-23-56.png" class="img" height="250" />

网页布局过程：
1. 先准备好相关的网页元素，网页元素基本都是盒子 Box 
2. 利用 CSS 设置好盒子样式，然后摆放到相应位置
3. 往盒子里面装内容

网页布局的核心本质： 就是利用 CSS 摆盒子

## 1.2 盒子模型（Box Model）组成

所谓 `盒子模型`：就是把 HTML 页面中的布局元素看作是一个矩形的盒子，也就是一个盛装内容的容器。

CSS 盒子模型本质上是一个盒子，封装周围的 HTML 元素，它包括：边框、外边距、内边距、和 实际内容

<img src="./images/YanCchen_2022-08-23_10-33-15.png" class="img" height="250" />

<img src="./images/YanCchen_2022-08-23_10-34-21.png" class="img" height="250" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=138&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对盒子模型组成的讲解

## 1.3 边框（border）

border可以设置元素的边框。边框有三部分组成:边框宽度(粗细) 边框样式 边框颜色

#### 语法：

```css
border : border-width || border-style || border-color
```

<img src="./images/YanCchen_2022-08-23_10-39-52.png" class="img" />

CSS 边框属性允许你指定一个元素边框的`样式`和`颜色`

边框样式 border-style 可以设置如下值：
- none：没有边框即忽略所有边框的宽度（默认值）
- solid：边框为单实线(最为常用的)
- dashed：边框为虚线 
- dotted：边框为点线

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=139&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对边框的讲解

#### 边框简写：

```css
border: 1px solid red; 没有顺序
```

#### 边框分开写法：

```css
border-top: 1px solid red; /* 只设定上边框， 其余同理 */ 
```

> 这里给和我一样不知道上下左右的
> - top 上 
> - bottom 下 
> - left 左 
> - right 右

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=140&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对边框简写的讲解

## 1.4 表格的细线边框

`border-collapse` 属性控制浏览器绘制表格边框的方式。它控制相邻单元格的边框

#### 语法：

```css
border-collapse:collapse;
```

- collapse 单词是合并的意思
- border-collapse: collapse; 表示相邻边框合并在一起

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=141&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对表格的细线边框的讲解

## 1.5 边框会影响盒子实际大小

边框会额外增加盒子的实际大小。因此我们有两种方案解决:
1. 测量盒子大小的时候,不量边框.
2. 如果测量的时候包含了边框,则需要 width/height 减去边框宽度

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=142&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对边框会影响盒子实际大小的讲解

## 1.6 内边距（padding）

`padding` 属性用于设置内边距，即边框与内容之间的距离

<img src="./images/YanCchen_2022-08-23_11-24-49.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=143&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对内边距的讲解

#### 简写:

`padding` 属性（简写属性）可以有一到四个值

<img src="./images/YanCchen_2022-08-23_11-25-38.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=144&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对内边距简写的讲解

?> 以上 4 种情况，我们实际开发都会遇到

当我们给盒子指定 padding 值之后，发生了 2 件事情：
1. 内容和边框有了距离，添加了内边距。
2. padding影响了盒子实际大小。

也就是说，如果盒子已经有了宽度和高度，此时再指定内边框，会撑大盒子

##### 解决方案：<br>
如果保证盒子跟效果图大小保持一致，则让 `width/height 减去多出来的内边距大小`即可

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=145&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

?> 如果盒子本身没有指定width/height属性, 则此时padding不会撑开盒子大小

## 1.7 外边距（margin）

`margin` 属性用于设置外边距，即控制盒子和盒子之间的距离

<img src="./images/YanCchen_2022-08-23_13-20-19.png" class="img" />

margin 简写方式代表的意义跟 [padding](/CSS基础/DISANTIAN?id=简写) 完全一致

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=150&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对外边距的讲解

### 外边距典型应用

外边距可以让块级盒子`水平居中`，但是必须满足两个条件：<br>
① 盒子必须指定了宽度（width）<br>
② 盒子`左右的外边距`都设置为 auto

```css
.header{ width:960px; margin:0 auto;}
```

常见的写法，以下三种都可以：
- margin-left: auto; margin-right: auto;
- margin: auto;
- `margin: 0 auto;`

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=151&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对外边距典型应用的讲解

!> 注意：以上方法是让块级元素水平居中，`行内元素或者行内块元素水平居中给其父元素添加 text-align:center 即可`

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=152&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.8 外边距合并

使用 `margin` 定义块元素的`垂直外边距`时，可能会出现外边距的合并

主要有两种情况:
1. [相邻块元素垂直外边距的合并](/CSS基础/DISANTIAN?id=_1-相邻块元素垂直外边距的合并)
2. [嵌套块元素垂直外边距的塌陷](/CSS基础/DISANTIAN?id=_2-嵌套块元素垂直外边距的塌陷)

### 1. 相邻块元素垂直外边距的合并

当上下相邻的两个块元素（兄弟关系）相遇时，如果上面的元素有下外边距 margin-bottom，下面的元素有
上外边距 margin-top ，则他们之间的垂直间距不是 margin-bottom 与 margin-top 之和。`取两个值中的较大者这种现象被称为相邻块元素垂直外边距的合并`

<img src="./images/YanCchen_2022-08-23_13-41-13.png" class="img" />

#### 解决方案：
`尽量只给一个盒子添加 margin 值`

### 2. 嵌套块元素垂直外边距的塌陷

对于两个嵌套关系（父子关系）的块元素，父元素有上外边距同时子元素也有上外边距，此时父元素会塌陷较大的外边距值

<img src="./images/YanCchen_2022-08-23_13-43-29.png" class="img" />

#### 解决方案：<br>
① 可以为父元素定义上边框<br>
② 可以为父元素定义上内边距<br>
③ `可以为父元素添加 overflow:hidden`

还有其他方法，比如浮动、固定，绝对定位的盒子不会有塌陷问题

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=153&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.9 清除内外边距

网页元素很多都带有默认的内外边距，而且不同浏览器默认的也不一致。因此我们在布局前，首先要清除下网页元素的内外边距

```css
* {
    padding:0; /* 清除内边距 */
    margin:0; /* 清除外边距 */
 }
```

!> 注意：`行内元素为了照顾兼容性，尽量只设置左右内外边距，不要设置上下内外边距。但是转换为块级和行内块元素就可以了`

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=154&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对清除内外边距的讲解

# **2. PS基本操作**

因为网页美工大部分效果图都是利用 `PS（Photoshop）`来做的，所以以后我们大部分切图工作都是在 `PS` 里面完成
- `文件 → 打开` ：可以打开我们要测量的图片
- `Ctrl+R`：可以打开标尺，或者 `视图 → 标尺`
- 右击标尺，把里面的单位改为`像素 `
- `Ctrl+ 加号(+)`可以放大视图， `Ctrl+ 减号(-)`可以缩小视图
- `按住空格键`，鼠标可以变成小手，拖动 PS 视图
- 用`选区`拖动 可以测量大小
- `Ctrl+ D` 可以取消选区，或者在`旁边空白处点击一下`也可以取消选区

<img src="./images/YanCchen_2022-08-23_14-08-16.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=155&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对PS基本操作的讲解

# **3. 综合案例**

## 案例1

<img src="./images/YanCchen_2022-08-23_14-55-33.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=156&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## Pink 老师总结

1. 布局为啥用不同盒子,我只想用div？<br>
标签都是有语义的, 合理的地方用合理的标签。比如产品标题 就用 h, 大量文字段落就用p

2. 为啥用辣么多类名？<br>
类名就是给每个盒子起了一个名字,可以更好的找到这个盒子, 选取盒子更容易,后期维护也方便

3. 到底用 margin 还是 padding？<br>
大部分情况两个可以混用，两者各有优缺点，但是根据实际情况，总是有更简单的方法实现

4. 自己做没有思路？<br>
布局有很多种实现方式，同学们可以开始先模仿我的写法，然后再做出自己的风格<br>
最后同学们一定多运用辅助工具,比如屏幕画笔,ps等等

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=161&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 案例2

<img src="./images/YanCchen_2022-08-23_15-08-57.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=162&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 去掉 li 前面的 项目符号(小圆点)

#### 语法：

```css
list-style: none;
```

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=164&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=125.8)可以观看pink老师的讲解

# **4. 圆角边框**

在 CSS3 中，新增了`圆角边框样式`，这样我们的盒子就可以变圆角了

`border-radius` 属性用于设置元素的外边框圆角

#### 语法：

```css
border-radius:length;
```

`radius半径（圆的半径）原理：`（椭）圆于边框的交集形成圆角效果

<img src="./images/YanCchen_2022-08-23_15-48-32.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=165&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对圆角边框的讲解

- 参数值可以为`数值`或`百分比`的形式
- 如果是`正方形`，想要设置为一个圆，把数值修改为`高度或者宽度的一半`即可，或者直接写为 `50%`
- `如果是个矩形，设置为高度的一半就可以了`
- 该属性是一个`简写属性`，可以跟四个值，分别代表`左上角`、`右上角`、`右下角`、`左下角`
- 分开写：`border-top-left-radius`、`border-top-right-radius`、`border-bottom-right-radius` 和`border-bottom-left-radius`
- `兼容性 ie9+ 浏览器支持, 但是不会影响页面布局,可以放心使用`

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=166&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对圆角边框的讲解

# **5. 盒子阴影**

CSS3 中新增了盒子阴影，我们可以使用 `box-shadow` 属性为盒子添加阴影

#### 语法：

```css
box-shadow: h-shadow v-shadow blur spread color inset;
```

<img src="./images/YanCchen_2022-08-23_16-09-30.png" class="img" />

!> 注意：<br>`1. 默认的是外阴影(outset), 但是不可以写这个单词,否则造成阴影无效`<br>`2. 盒子阴影不占用空间，不会影响其他盒子排列`

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=167&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对盒子阴影的讲解

# **6. 文字阴影**

在 CSS3 中，我们可以使用 `text-shadow` 属性将阴影应用于文本

#### 语法：

```css
text-shadow: h-shadow v-shadow blur color;
```

<img src="./images/YanCchen_2022-08-23_16-23-22.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=168&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对文字阴影的讲解

