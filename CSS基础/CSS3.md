
## 1.1 CSS3的现状

- 新增的CSS3特性有兼容性问题，ie9+才支持
- 移动端支持优于 PC 端
- 不断改进中
- 应用相对广泛
- 现阶段主要学习：<hong>新增选择器</hong>和<hong>盒子模型</hong>以及<hong>其他特性</hong>

##### CSS3 新增选择器

CSS3 给我们新增了选择器，可以更加便捷，更加自由的选择目标元素
1. 属性选择器
2. 结构伪类选择器
3. 伪元素选择器

## 1.2 属性选择器

属性选择器可以根据元素特定属性的来选择元素。 这样就可以不用借助于类或者id选择器

<img src="./images/YanCchen_2022-09-04_07-07-24.png" class="img" height="300" />

!> <hong>注意：类选择器、属性选择器、伪类选择器，权重为 10</hong>

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=280&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.3 结构伪类选择器

结构伪类选择器主要根据<hong>文档结构</hong>来选择器元素， 常用于根据父级选择器里面的子元素

<img src="./images/YanCchen_2022-09-04_07-25-18.png" class="img" height="300" />

!> <hong>注意：类选择器、属性选择器、伪类选择器，权重为 10</hong>

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=282&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

**nth-child（n）** 选择某个父元素的一个或多个特定的子元素（重点）

- <hong>n 可以是数字，关键字和公式</hong>
- n 如果是数字，就是选择第 n 个子元素， 里面数字从1开始…
- n 可以是关键字：even 偶数，odd 奇数
- n 可以是公式：常见的公式如下 ( 如果n是公式，则从0开始计算，但是第 0 个元素或者超出了元素的个数会被忽略 )

<img src="./images/YanCchen_2022-09-04_07-27-25.png" class="img" />

结构伪类选择器主要根据<hong>文档结构</hong>来选择器元素， 常用于根据父级选择器里面的子元素

<img src="./images/YanCchen_2022-09-04_07-25-18.png" class="img" height="300" />

<hong>区别：</hong><br>
<hong>1. nth-child 对父元素里面所有孩子排序选择（序号是固定的） 先找到第n个孩子，然后看看是否和E匹配</hong><br>
<hong>2. nth-of-type 对父元素里面指定子元素进行排序选择。 先去匹配E ，然后再根据E 找第n个孩子</hong>

### 小结

- 结构伪类选择器一般用于选择父级里面的第几个孩子
- nth-child 对父元素里面所有孩子排序选择（序号是固定的） 先找到第n个孩子，然后看看是否和E匹配
- nth-of-type 对父元素里面指定子元素进行排序选择。 先去匹配E ，然后再根据E 找第n个孩子
- 关于 nth-child（n） 我们要知道 n 是从 0 开始计算的，要记住常用的公式
- 如果是无序列表，我们肯定用 nth-child 更多
- 类选择器、属性选择器、伪类选择器，权重为 10

## 1.4 伪元素选择器

伪元素选择器可以帮助我们利用CSS创建新标签元素，而不需要HTML标签，从而简化HTML结构

<img src="./images/YanCchen_2022-09-04_16-02-58.png" class="img" />

```css
div::before {
    content: '';
}
```

!> <hongcu>注意：</hongcu><br>
● <hong>before</hong> 和 <hong>after</hong> 创建一个元素，但是属于行内元素<br>
● 新创建的这个元素在文档树中是找不到的，所以我们称为<hong>伪元素</hong><br>
● <hong>语法： element::before {} </hong><br>
● before 和 after 必须有 <hong>content 属性</hong><br>
● before 在父元素内容的前面创建元素，after 在父元素内容的后面插入元素<br>
● <hong>伪元素选择器</hong>和<hong>标签选择器</hong>一样，权重为 1

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=286&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.5 CSS3盒子模型

CSS3 中可以通过 <hong>box-sizing</hong> 来指定盒模型，有2个值：即可指定为 <hong>content-box</hong>、<hong>border-box</hong>，这样我们计算盒子大小的方式就发生了改变

可以分成两种情况：
1. box-sizing: content-box 盒子大小为 width + padding + border （以前默认的）
2. box-sizing: border-box 盒子大小为 width

如果盒子模型我们改为了box-sizing: border-box ， 那padding和border就不会撑大盒子了（前提padding和border不会超过width宽度）

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=291&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.6 CSS3其他特性(了解)

1. 图片变模糊
2. 计算盒子宽度 width: calc 函数

### CSS3滤镜filter:

filter CSS属性将模糊或颜色偏移等图形效果应用于元素

```css
filter: 函数(); 例如： filter: blur(5px); blur模糊处理 数值越大越模糊
```

<img src="./images/YanCchen_2022-09-04_16-43-53.png" class="img" height="200" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=292&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### CSS3 calc 函数:

calc() 此CSS函数让你在声明CSS属性值时执行一些计算

```css
width: calc(100% - 80px);
```

括号里面可以使用 + - * / 来进行计算

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=293&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

## 1.7 CSS3过渡

过渡（transition)是CSS3中具有颠覆性的特征之一，我们可以在不使用 Flash 动画或JavaScript 的情况下，当元素从一种样式变换为另一种样式时为元素添加效果

过渡动画： 是从一个状态 渐渐的过渡到另外一个状态

可以让我们页面更好看，更动感十足，虽然 低版本浏览器不支持（ie9以下版本） 但是不会影响页面布局

<hong>我们现在经常和 :hover 一起 搭配使用</hong>

```css
transition: 要过渡的属性 花费时间 运动曲线 何时开始;
```

**1. 属性 ：** 想要变化的 css 属性， 宽度高度 背景颜色 内外边距都可以 。如果想要所有的属性都变化过渡， 写一个all 就可以<br>
**2. 花费时间：** 单位是 秒（必须写单位） 比如 0.5s <br>
**3. 运动曲线：** 默认是 ease （可以省略）<br>
**4. 何时开始 ：**单位是 秒（必须写单位）可以设置延迟触发时间 默认是 0s （可以省略）

<img src="./images/YanCchen_2022-09-04_16-58-45.png" class="img" height="200" />

<hong>记住过渡的使用口诀： 谁做过渡给谁加</hong>

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=293&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解