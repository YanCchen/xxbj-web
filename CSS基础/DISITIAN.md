## 哈哈

# **1. 浮动（float)**

## 1.1 传统网页布局的三种方式

网页布局的本质——用 CSS 来摆放盒子。 把盒子摆放到相应位置

CSS 提供了三种传统布局方式(简单说,就是盒子如何进行排列顺序)：
- 普通流（标准流）
- 浮动
- 定位

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=170&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对传统网页布局的三种方式的讲解

## 1.2 标准流（普通流/文档流）

<hong>所谓的标准流: 就是标签按照规定好默认方式排列</hong>

> 1. 块级元素会独占一行，从上向下顺序排列
> - 常用元素：div、hr、p、h1~h6、ul、ol、dl、form、table
> 2. 行内元素会按照顺序，从左到右顺序排列，碰到父元素边缘则自动换行
> - 常用元素：span、a、i、em 等

以上都是标准流布局，我们前面学习的就是标准流，<hong>标准流是最基本的布局方式</hong>

这三种布局方式都是用来摆放盒子的，盒子摆放到合适位置，布局自然就完成了

!> <hong>注意：实际开发中，一个页面基本都包含了这三种布局方式</hong>

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=170&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=73.3)可以观看pink老师对标准流的讲解

## 1.3 为什么需要浮动？

提问：我们用标准流能很方便的实现如下效果吗？

1. 如何让多个块级盒子(div)水平排列成一行？

<img src="./images/YanCchen_2022-08-24_10-44-33.png" class="img" />

比较难，虽然转换为行内块元素可以实现一行显示，但是他们之间会有大的空白缝隙，很难控制

提问：我们用标准流能很方便的实现如下效果吗？

2. 如何实现两个盒子的左右对齐？

<img src="./images/YanCchen_2022-08-24_10-45-55.png" class="img" />

总结： 有很多的布局效果，标准流没有办法完成，此时就可以利用浮动完成布局。 因为浮动可以改变元素标签默认的排列方式

浮动最典型的应用：可以让多个块级元素一行内排列显示

网页布局第一准则：<hong>多个块级元素纵向排列找标准流，多个块级元素横向排列找浮动</hong>

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=171&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对为什么需要浮动的讲解

## 1.4 什么是浮动？

<hong>float</hong> 属性用于创建浮动框，将其移动到一边，直到左边缘或右边缘触及包含块或另一个浮动框的边缘

#### 语法：

```css
选择器 { float: 属性值; }
```

<img src="./images/YanCchen_2022-08-24_10-55-46.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=172&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师对什么是浮动的讲解

## 1.5 浮动特性

加了浮动之后的元素,会具有很多特性,需要我们掌握的<br>
<hong>1. 浮动元素会脱离标准流(脱标)</hong><br>
2. 浮动的元素会一行内显示并且元素顶部对齐<br>
3. 浮动的元素会具有行内块元素的特性

### 1. 浮动元素会脱离标准流(脱标)

设置了浮动（float）的元素最重要特性：
1. 脱离标准普通流的控制（浮） 移动到指定位置（动）, （俗称<hong>脱标</hong>）
2. 浮动的盒子<hong>不再保留原先的位置</hong>

<img src="./images/YanCchen_2022-08-24_11-13-45.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=173&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 2. 浮动的元素会一行内显示并且元素顶部对齐

 如果多个盒子都设置了浮动，则它们会按照属性值<hong>一行内显示并且顶端对齐排列</hong>
 
<img src="./images/YanCchen_2022-08-24_11-15-41.png" class="img" />

!> <hong>注意： 浮动的元素是互相贴靠在一起的（不会有缝隙），如果父级宽度装不下这些浮动的盒子， 多出的盒子会另起一行对齐</hong>

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=174&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 3. 浮动的元素会具有行内块元素的特性

任何元素都可以浮动。不管原先是什么模式的元素，添加浮动之后具有<hong>行内块元素</hong>相似的特性
- 如果块级盒子没有设置宽度，默认宽度和父级一样宽，但是添加浮动后，它的大小根据内容来决定
- 浮动的盒子中间是没有缝隙的，是紧挨着一起的
- 行内元素同理

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=175&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.6 浮动元素经常和标准流父级搭配使用

为了约束浮动元素位置, 我们网页布局一般采取的策略是:

<hong>先用标准流的父元素排列上下位置, 之后内部子元素采取浮动排列左右位置. 符合网页布局第一准侧</hong>

<img src="./images/YanCchen_2022-08-24_11-29-20.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=176&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 案例

- [案例一](/CSS基础/DISITIAN?id=案例一)
- [案例二](/CSS基础/DISITIAN?id=案例二)
- [案例三](/CSS基础/DISITIAN?id=案例三)
- [小小总结](/CSS基础/DISITIAN?id=小小总结)

### 案例一

<img src="./images/YanCchen_2022-08-24_12-22-20.png" class="img" />

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box {
            width: 1200px;
            height: 460px;
            background-color: pink;
            margin: 0 auto;
        }
        .left {
            float: left;
            width: 230px;
            height: 460px;
            background-color: blueviolet;
        }
        .right {
            float: left;
            width: 970px;
            height: 460px;
            background-color: aqua;
        }
    </style>
</head>
<body>
    <div class="box">
        <div class="left">左侧</div>
        <div class="right">右侧</div>
    </div>
</body>
</html>
```

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=177&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 案例二

<img src="./images/YanCchen_2022-08-24_12-32-42.png" class="img" />

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }
        li {
            list-style: none;
        }
        .box {
            width: 1226px;
            height: 285px;
            background-color: pink;
            /* margin 居中对齐 */
            margin: 0 auto;
        }
        .box li {
            width: 296px;
            height: 285px;
            background-color: blueviolet;
            /* 添加浮动 */
            float: left;
            /* 设置右外边距 14px */
            margin-right: 14px;
        }
        /* 这里不能直接写.last，不然权重不够不起效 */
        .box .last {
            /* 因为父盒子不够大，第四个盒子被挤下来了，而且第四个盒子不需要置右外边距，所以第四个盒子的右边距清零 */
            margin-right: 0;
        }
    </style>
</head>
<body>
    <ul class="box">
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li class="last">4</li>
    </ul>
</body>
</html>
```

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=178&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 案例三

<img src="./images/YanCchen_2022-08-24_12-55-26.png" class="img" />

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box {
            width: 1226px;
            height: 615px;
            background-color: pink;
            margin: 0 auto;
        }
        .left {
            float: left;
            width: 234px;
            height: 615px;
            background-color: blueviolet;
        }
        .right {
            float: left;
            width: 992px;
            height: 615px;
            background-color: aqua;
        }
        .right>div {
            float: left;
            width: 234px;
            height: 300px;
            background-color: pink;
            margin-left: 14px;
            margin-bottom: 14px;
        }
    </style>
</head>
<body>
    <div class="box">
        <div class="left">左青龙</div>
        <div class="right">
            <div>1</div>
            <div>2</div>
            <div>3</div>
            <div>4</div>
            <div>5</div>
            <div>6</div>
            <div>7</div>
            <div>8</div>
        </div>
    </div>
</body>
</html>
```

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=179&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 小小总结

<hong>网页布局第二准侧</hong>
- <hong>先设置盒子的大小, 之后设置盒子的位置</hong>

# **2. 常见网页布局**

## 2.1 常见网页布局

<img src="./images/YanCchen_2022-08-24_13-19-06.png" class="img" />
<img src="./images/YanCchen_2022-08-24_13-19-29.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=181&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 2.2 浮动布局注意点

1. **浮动和标准流的父盒子搭配**

<hong>先用标准流的父元素排列上下位置, 之后内部子元素采取浮动排列左右位置</hong>

2. **一个元素浮动了，理论上其余的兄弟元素也要浮动**

一个盒子里面有多个子盒子，如果其中一个盒子浮动了，那么其他兄弟也应该浮动，以防止引起问题

<hong>浮动的盒子只会影响浮动盒子后面的标准流,不会影响前面的标准流</hong>

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=182&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 思考题

### 思考题:

我们前面浮动元素有一个标准流的父元素, 他们有一个共同的特点,都是有高度的<br>
但是, 所有的父盒子都必须有高度吗?

<img src="./images/YanCchen_2022-08-24_13-50-33.png" class="img" />

我们前面浮动元素有一个标准流的父元素, 他们有一个共同的特点,都是有高度的<br>
但是, 所有的父盒子都必须有高度吗? <br>
理想中的状态, 让子盒子撑开父亲. 有多少孩子,我父盒子就有多高<br>
但是不给父盒子高度会有问题吗?…..

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=183&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **3. 清除浮动**

## 3.1 为什么需要清除浮动？

由于父级盒子很多情况下，不方便给高度，但是子盒子浮动又不占有位置，最后父级盒子高度为 0 时，就会影响下面的标准流盒子

<img src="./images/YanCchen_2022-08-24_14-00-54.png" class="img" />

- 由于浮动元素不再占用原文档流的位置，所以它会对后面的元素排版产生影响

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=183&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=474.7)可以观看pink老师的讲解

## 3.2 清除浮动本质

- 清除浮动的本质是清除浮动元素造成的影响
- 如果父盒子本身有高度，则不需要清除浮动
- <hong>清除浮动之后，父级就会根据浮动的子盒子自动检测高度。父级有了高度，就不会影响下面的标准流了</hong>

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=184&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 3.3 清除浮动

#### 语法：

```css
选择器{clear:属性值;}
```

<img src="./images/YanCchen_2022-08-24_14-07-09.png" class="img" />

我们实际工作中， 几乎只用 <hong>clear: both;</hong>

<hong>清除浮动的策略是: 闭合浮动</hong>

#### 清除浮动方法

1.**额外标签法**也称为隔墙法，是 **W3C 推荐的做法**<br>
<hong>2.父级添加 overflow 属性</hong><br>
<hong>3.父级添加after伪元素</hong><br>
<hong>4.父级添加双伪元素</hong>

> 内容较多，点击导航
> - [清除浮动 —— 额外标签法](/CSS基础/DISITIAN?id=清除浮动-额外标签法)
> - [清除浮动 —— 父级添加 overflow](/CSS基础/DISITIAN?id=清除浮动-父级添加-overflow)
> - [清除浮动 —— :after 伪元素法](/CSS基础/DISITIAN?id=清除浮动-伪元素法)
> - [清除浮动 —— 双伪元素清除浮动](/CSS基础/DISITIAN?id=清除浮动-双伪元素清除浮动)
> - [清除浮动总结](/CSS基础/DISITIAN?id=清除浮动总结)

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=184&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=59.9)可以观看pink老师的讲解

### 清除浮动 —— 额外标签法

<hongcu>额外标签法</hongcu>也称为<hong>隔墙法</hong>，是 W3C 推荐的做法

<hong>额外标签法</hong>会在浮动元素末尾添加一个空的标签。例如 &lt;div style=”clear:both”>&lt;/div>，或者其他标签
（如&lt;br />等）
- 优点： 通俗易懂，书写方便
- 缺点： 添加许多无意义的标签，结构化较差

!> <hong>注意： 要求这个新的空标签必须是块级元素<hong>

#### 总结:

1. 清除浮动本质是? 

<hong>清除浮动的本质是清除浮动元素脱离标准流造成的影响</hong>

2. 清除浮动策略是?

<hong>闭合浮动. 只让浮动在父盒子内部影响,不影响父盒子外面的其他盒子</hong>

3. 额外标签法?

<hong>隔墙法, 就是在最后一个浮动的子元素后面添加一个额外标签, 添加 清除浮动样式</hong><br>
<hong>实际工作可能会遇到,但是不常用</hong>

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=184&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=171.9)可以观看pink老师的讲解

### 清除浮动 —— 父级添加 overflow

可以给父级添加 <hong>overflow</hong> 属性，将其属性值设置为 <hong>hidden</hong>、 <hong>auto</hong> 或 <hong>scroll</hong>

子不教,父之过,注意是给父元素添加代码
- 优点：代码简洁
- 缺点：无法显示溢出的部分

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=185&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 清除浮动 —— :after 伪元素法

<hong>:after</hong> 方式是额外标签法的升级版。也是给父元素添加

```css
.clearfix:after { 
    content: ""; 
    display: block; 
    height: 0; 
    clear: both; 
    visibility: hidden; 
} 
.clearfix { 
    /* IE6、7 专有 */ 
    *zoom: 1;
}
```

- 优点：没有增加标签，结构更简单
- 缺点：照顾低版本浏览器
- 代表网站： 百度、淘宝网、网易等

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=186&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 清除浮动 —— 双伪元素清除浮动

也是给给父元素添加

```css
.clearfix:before,
.clearfix:after {
    content:"";
    display:table; 
}
.clearfix:after {
    clear:both;
}
.clearfix {
    *zoom:1;
}
```

- 优点：代码更简洁
- 缺点：照顾低版本浏览器
- 代表网站：小米、腾讯等

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=187&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 清除浮动总结

**为什么需要清除浮动？**<br>
① 父级没高度<br>
② 子盒子浮动了<br>
③ 影响下面布局了，我们就应该清除浮动了

<img src="./images/YanCchen_2022-08-24_14-51-21.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=188&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **4. PS切图**

PS 有很多的切图方式：图层切图、切片切图、PS 插件切图等

### 常见的图片格式

<img src="./images/YanCchen_2022-08-24_15-00-06.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=189&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 4.1 图层切图

最简单的切图方式：右击图层 → 导出 PNG 切片

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=190&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

但是很多情况下，我们需要合并图层再导出：

1. 选中需要的图层：图层菜单 → 合并图层（也可以使用快捷键：Ctel+e）
2. 右击 → 快速导出为PNG 

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=191&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 4.2 切片切图

**1. 利用切片选中图片**

- 利用切片工具手动划出

**2. 导出选中的图片**

文件菜单 → 存储为 web 设备所用格式 → 选择我们要的图片格式 → 存储

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=192&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 4.3 PS 插件切图

<hong>Cutterman</hong> 是一款运行在 <hong>Photoshop</hong> 中的插件，能够自动将你需要的图层进行输出，以替代传统的手工"导出 web 所用格式" 以及使用切片工具进行挨个切图的繁琐流程

官网：http://www.cutterman.cn/zh/cutterman

!> <hong>注意：Cutterman 插件要求你的 PS 必须是完整版，不能是绿色版，所以大家需要安装完整版本</hong>

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=193&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

# **5. 学成在线案例**

<img src="./images/YanCchen_2022-08-24_19-06-35.png" class="img" />

## 5.1 准备素材和工具

1. 学成在线 PSD 源文件
2. 开发工具 = PS（切图） + sublime（代码） + chrome（测试）

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=195&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.2 案例准备工作

我们本次采取结构与样式相分离思想：
1. 创建 study 目录文件夹 (用于存放我们这个页面的相关内容)
2. study 目录内新建 images 文件夹，用于保存图片
3. 新建首页文件 index.html（以后我们的网站首页统一规定为 index.html )
4. 新建 style.css 样式文件。我们本次采用外链样式表
5. 将样式引入到我们的 HTML 页面文件中
6. 样式表写入清除内外边距的样式，来检测样式表是否引入成功

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=195&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=112.5)可以观看pink老师的讲解

## 5.3 CSS 属性书写顺序

建议遵循以下顺序：
1. 布局定位属性：display / position / float / clear / visibility / overflow（建议 display 第一个写，毕竟关系到模式）
2. 自身属性：width / height / margin / padding / border / background
3. 文本属性：color / font / text-decoration / text-align / vertical-align / white- space / break-word
4. 其他属性（CSS3）：content / cursor / border-radius / box-shadow / text-shadow / background:linear-gradient…

例如：

```css
.jdc {
    /* 布局定位属性 */
    display: block;
    position: relative;
    float: left;
    /* 自身属性 */
    width: 100px;
    height: 100px;
    margin: 0 10px;
    padding: 20px 0;
    /* 文本属性 */
    font-family: Arial, 'Helvetica Neue', Helvetica, sans-serif;
    color: #333;
    /* 其他属性 */
    background: rgba(0,0,0,.5);
    border-radius: 10px;
}
```

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=196&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.4 页面布局整体思路

为了提高网页制作的效率，布局时通常有以下的整体思路：
1. 必须确定页面的版心（可视区），我们测量可得知。
2. 分析页面中的行模块，以及每个行模块中的列模块。其实页面布局第一准则
3. 一行中的列模块经常浮动布局，先确定每个列的大小，之后确定列的位置。页面布局第二准则
4. 制作 HTML 结构。我们还是遵循，先有结构，后有样式的原则。结构永远最重要
5. 所以，先理清楚<hong>布局结构</hong>，再写代码尤为重要。这需要我们多写多积累

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=197&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.5 确定版心

这个页面的版心是 1200 像素，每个版心都要水平居中对齐，可以定义版心为公共类：

```css
.w {
    width: 1200px;
    margin: auto;
}
```

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=198&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.6 头部制作

<img src="./images/YanCchen_2022-08-24_19-41-12.png" class="img" />

- 1 号是版心盒子 header 1200 * 42 的盒子水平居中对齐，上下给一个 margin 值就可以
- 版心盒子里面包含 2 号盒子 logo
- 版心盒子里面包含 3 号盒子 nav 导航栏
- 版心盒子里面包含 4 号盒子 search 搜索框
- 版心盒子里面包含 5 号盒子 user 个人信息
- 注意：要求里面的 4 个盒子必须都是浮动

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=198&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

**导航栏注意点:**

<hong>实际开发中，我们不会直接用链接a 而是用 li 包含链接(li+a)的做法</hong>
1. li+a 语义更清晰，一看这就是有条理的列表型内容
2. 如果直接用a，搜索引擎容易辨别为有堆砌关键字嫌疑（故意堆砌关键字容易被搜索引擎有降权的风险），从而影响网站排名

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=200&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

!> **注意:**<br>1. 让导航栏一行显示, 给 li 加浮动, 因为 li 是块级元素, 需要一行显示<br>2. 这个nav导航栏可以不给宽度,将来可以继续添加其余文字<br>3. 因为导航栏里面文字不一样多,所以最好给链接 a 左右padding 撑开盒子,而不是指定宽度

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=201&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

search 搜索框:
一个 search 大盒子里面包含 2个 表单

<img src="./images/YanCchen_2022-08-25_11-25-57.png" class="img" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=203&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.7 banner 制作

<img src="./images/YanCchen_2022-08-25_12-17-39.png" class="img" />

- 1 号盒子是通栏的大盒子 banner，不给宽度，给高度，给一个蓝色背景
- 2 号盒子是版心，要水平居中对齐
- 3 号盒子版心内，左对齐 subnav 侧导航栏
- 4 号盒子版心内，右对齐 course 课程

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=206&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.8 精品推荐小模块

<img src="./images/YanCchen_2022-08-25_12-51-05.png" class="img" />

- 大盒子水平居中 goods 精品，注意此处有个盒子阴影
- 1 号盒子是标题 H3 左侧浮动
- 2 号盒子里面放链接左侧浮动， goods-item 距离可以控制链接的左右内边距（注意行内元素只给左右内外边距）
- 3 号盒子右浮动 mod 修改

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=212&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.9 精品推荐大模块

<img src="./images/YanCchen_2022-08-25_13-52-56.png" class="img" />

- 1 号盒子为最大的盒子， box 版心水平居中对齐
- 2 号盒子为上面部分，box-hd -- 里面左侧标题 H3 左浮动，右侧链接 a 右浮动
- 3 号盒子为底下部分，box-bd -- 里面是无序列表，有 10 个小 li 组成
- 小 li 外边距的问题，这里有个小技巧：给 box-hd 宽度为 1225 就可以一行装开 5 个 li

复习点：我们用到清除浮动，因为 box-hd 里面的盒子个数不一定是多少，所以我们就不给高度了，但是里面的盒子浮动会影响下面的布局，因此需要清除浮动

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=215&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 5.10 底部模块

<img src="./images/YanCchen_2022-08-25_14-02-35.png" class="img" />

- 1 号盒子是通栏大盒子，底部 footer 给高度，底色是白色
- 2 号盒子版心水平居中
- 3 号盒子版权 copyright 左对齐
- 4 号盒子链接组 links 右对齐

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=218&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解