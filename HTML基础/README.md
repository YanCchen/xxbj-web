## 哈哈

# **1.HTML语法规范**

## 1.1基本语法概述

1. HTML标签是`由尖括号包围的关键词`，例如`<html>`
2. HTML标签`通常是成对出现的`，例如`<html>`和`</html>`,我们称为`双标签。`标签对中的第一个标签是开始标签，第二个标签是结束标签。

> 如`<html>`这个是开始标签，`</html>`是结束标签，两者对比，结束标签前面多了个`/`

3. 有些特殊的标签必须是单个标签（极少情况），例如`<br />`，我们称为`单标签。`

## 1.2标签关系

双标签关系可以分为两类：`包含关系`和`并列关系`

#### 包含关系

```html
<head>
    <title> </title>
</head>
```

> 你可以把`包含关系`可以理解为`父子关系`

> `<head>`是父亲，`<title>`是儿子

<img src="./images/YanCchen_2022-08-18_12-34-54.png" class="img" />

#### 并列关系

```html
<head></head>
<body></body>
```

> 你可以把`并列关系`可以理解为`兄弟关系`


<img src="./images/微信图片_20221104161455.jpg" class="img" height="300"/>
<img src="./images/YanCchen_2022-08-18_12-47-36.png" class="img" />


# **2.HTML基本结构标签**

## 2.1第一个HTML网页

每一个网页都会有一个基本的结构标签（也称为骨架标签），页面内容也是在这些基本标签上书写。

HTML页面也称为HTML文档
```html
<html>
    <head>
        <title>我的第一个页面</title>
    </head>
    <body>
        你我之间，黑马洗练，月薪过万，一飞冲天
    </body>
</html>
```

|标签名|定义|说明  |
|:-------:|:--:|:---------|
|`<html></html>`|HTML标签|页面中最大的标签，我们称为`根标签`|
|`<head></head>`|文档的头部|注意在`head`标签中我们`必须要`设置的标签是`title`|
|`<title></title>`|文档的标题|让页面拥有一个属于自己的`网页标题`|
|`<body></body>`|文档的主题|元素包含文档的所有内容，`页面内容`基本都是放到`body`里面的|

<img src="./images/YanCchen_2022-08-18_13-22-41.png" class="img" />

> HTML文档的后缀名必须是`.html`或`.htm`，浏览器的作用是读取HTML文档，并以网页的形式显示出它们。

## 2.2基本结构标题总结

<img src="./images/YanCchen_2022-08-18_13-32-10.png" class="img" />

**下面请小猪佩奇来让我们更简单的理解**

<img src="./images/YanCchen_2022-08-18_13-34-36.png" class="img" />

# **3.网页开发工具**

#### 使用VSCode工具生成骨架标签新增代码

> 输入`!`，然后按`Tab`键就生成html骨架

1. `<!DOCTYPE>`标签
2. `lang`语言
3. `charset`字符串

## 3.1文档类型声明标签

`<!DOCTYPE>`文档类型声明，作用就是告诉浏览器使用哪种HTML版本来显示网页
```html
<!DOCTYPE html>
```
> 这句代码的意思是：当前页面采取的是HTML5版本来显示网页

> 注意：
> 1. `<!DOCTYPE>`声明位于文档中的最前面的位置，处于`<html>`标签之前
> 2. `<!DOCTYPE>`不是一个HTML标签，它就是文档类型声明标签

## 3.2lang语言种类

用来定义当前文档显示的语言

1. `en`定义语言为英语
2. `zh-CN`定义语言为中文

```html
<html lang="zh-CN">
```

通过上面的代码，可以了解这个网页定义为zh-CN中文网页，如果把zh-CN换成en,那就是定义为英文网页

其实对于文档显示来说，定义成en的文档也可以显示中文，定义成zh-CN的文档也可以显示中文

这个属性对浏览器和搜索引擎（百度.谷歌等）还是有作用的

## 字符集

字符集(character set)是多个字符的集合。以便计算机能够识别和储存各种文字

在`<head>`标签内，可以通过`<meta>`标签的`charset`属性来规定HTML文档应该使用哪种字符编码

```html
<meta charset="UTF-8" />
```

`charset`常用的值有：GB2312、BIG5、GBK和UTF-8，其中`UTF-8`也被称为万国码，基本包含了全世界所有国家需要用到的字符

> 注意：上面语法是必须要写的代码，否则可能引起乱码的情况。一般情况下，统一使用"`UTF-8`"编码，尽量统一写成标准的"UTF-8"，不要写成"utf8"或"UTF8"

# **4.HTML常用标签**

## 4.1标签语义

学习标签是有技巧的，重点是记住每个标签的语义。简单理解就是指`标签的含义`，即这个标签是用来干嘛的

> 根据标签的语义，在合适的地方给一个最为合理的标签，可以让页面结构更清晰

下面是没有加语义标签和加了语义标签的对比

<img src="./images/YanCchen_2022-08-18_15-29-06.png" class="img" />

## 4.2标题标签

为了使网页更具有语义化，我们经常会在页面中用到标题标签，HTML提供了6个等级的网页标题，即`<h1>`-`<h6>`

#### 语法格式：
```html
<h1>我是一级标题</h1>
```
单词head的缩写，意为头部、标题

> `标题语义：`作为标题使用，并且根据重要性递减

#### 特点：

1. 加了标题的文字会变的加粗，字号也会依次变大
2. 一行标题独占一行

#### 演示：
```html
<h1>我是一级标题</h1>
<h2>我是二级标题</h2>
<h3>我是三级标题</h3>
<h4>我是四级标题</h4>
<h5>我是五级标题</h5>
<h6>我是六级标题</h6>
```

**效果：**
<h1>我是一级标题</h1>
<h2>我是二级标题</h2>
<h3>我是三级标题</h3>
<h4>我是四级标题</h4>
<h5>我是五级标题</h5>
<h6>我是六级标题</h6>

## 4.3段落和换行标签

#### 1.段落标签

在网页中，要把文字有条理地显示出来，就需要将这些文字分段。在HTML标签中，`<p>`标签用于`定义段落`，它可以将整个网页分为若干个段落

#### 语法格式：
```html
<p>我是一个段落标签</p>
```

单词paragraph的缩写，意为段落

> `标签语义：`可以把HTML文档分割为若干段落

#### 特点：

1. 文本在一个段落中会根据浏览器窗口的大小自动换行
2. 段落和段落之间保有空隙

#### 演示：
```html
<p>我是Yan</p>
<p>我来自梧州</p>
<p>我很喜欢摸鱼</p>
```

**效果：**

<p>我是Yan</p>
<p>我来自梧州</p>
<p>我很喜欢摸鱼</p>

#### 2.换行标签

在HTML中，一个段落中的文字会从左到右依次排列，直到浏览器窗口的右端，然后才自动换行。<br />如果希望某段文本强制换行显示，就需要使用`换行标签` `<br />`

#### 语法格式：
```html
<br />
```

单词break的缩写，意为打断、换行

> `标签语义：`强制换行

#### 特点：

1. `<br />`是个单标签
2. `<br />`标签只是简单地开始新的一行，跟段落不一样，段落之间会插入一些垂直的间距

#### 演示：
```html
我是Yan<br />我来自梧州<br />我很喜欢摸鱼
```

**效果：**

我是Yan<br />我来自梧州<br />我很喜欢摸鱼

## 4.4文本格式化标签

在网页中，有时需要为文字设置<strong>`粗体`</strong>、<em>`斜体`</em>或<u>`下划线`</u>等效果，这时就需要用到HTML中的文本格式化标签，使文字以特殊的方式显示

#### 语法格式：
```html
<strong>加粗</strong>
<em>倾斜</em>
<del>删除线</del>
<ins>下航线</ins>
```

|语义|标签|
|:-------|:--|
|加粗|`<strong></strong>`或者`<b></b>`|
|倾斜|`<em></em>`或者`<i></i>`|
|删除线|`<del></del>`或者`<s></s>`|
|下划线|`<ins></ins>`或者`<u></u>`|

> `标签语义：`突出重要性，比普通文字更重要

#### 演示：
```html
<strong>我是加粗</strong>
<em>我是倾斜</em>
<del>我是删除线</del>
<ins>我是下航线</ins>
```

**效果：**

<strong>我是加粗</strong>
<em>我是倾斜</em>
<del>我是删除线</del>
<ins>我是下航线</ins>

## 4.5&lt;div&gt;和&lt;span&gt;标签

`<div>`和`<span>`是没有语义的，它们就是一个盒子，用来装内容的

#### 语法格式：
```html
<div>这是头部</div>
<span>今日价格</span>
```

div是division的缩写，表示分割、分区<br />span意为跨度，跨越

#### 特点：

1. `<div>`标签用来布局，但是现在一行只能放一个`<div>`。大盒子
2. `<span>`标签用来布局，一行上可多个`<span>`。小盒子

#### 演示：
```html
<div>我是div大哥</div>
<div>我是div二哥</div>
<div>我是div三哥</div>
<span>我是span大哥</span>
<span>我是span二哥</span>
<span>我是span三哥</span>
```

**效果：**

<div>我是div大哥</div>
<div>我是div二哥</div>
<div>我是div三哥</div>
<span>我是span大哥</span>
<span>我是span二哥</span>
<span>我是span三哥</span>

## 4.6图像标签和路径

### 1.图像标签

在HTML标签中，`<img>`标签用于定义HTML页面中的图像

#### 语法格式：

```html
<img src="图像URL" />
```

单词image的缩写，意为图像

> `src`是`<img>`标签中的`必须属性`，它用于`指定图像文件的路径和文件名`
> - 所谓属性：简单理解就是属于这个图像标签的特性

##### 图像标签的其他属性：

|属性|属性值|说明|
|:-------|:--|:--|
|src|图片路径|必须属性|
|alt|文本|替换文本。图像不能显示的文字|
|title|文本|提示文本。鼠标放到图像上，显示的文字|
|width|像素|设置图像的宽度|
|height|像素|设置图像的高度|
|border|像素|设置图像的边框粗细|

#### 演示：

> 这里演示添加了`alt`和`title`的用法

```html
<h6>图像标签的使用：</h6>
<img src="https://yjf.vin/static/picture/1.jpg" />
<h6>alt 替换文本 图像显示不出来的时候用文字替换：</h6>
<img src="https://yjf.vin/static/picture/11.jpg" alt="这是Yan的头像呀" />
<h6>title 提示文本 鼠标放到图像上，提示文字</h6>
<img src="https://yjf.vin/static/picture/1.jpg" title="这是Yan的头像呀" />
```

**效果：**

<h6>图像标签的使用：</h6>
<img src="https://yjf.vin/static/picture/1.jpg" />
<h6>alt 替换文本 图像显示不出来的时候用文字替换：</h6>
<img src="https://yjf.vin/static/picture/11.jpg" alt="这是Yan的头像呀" />
<h6>title 提示文本 鼠标放到图像上，提示文字</h6>
<img src="https://yjf.vin/static/picture/1.jpg" title="这是Yan的头像呀" />

#### - 各位有没有发现上面的图片特别大，那么我们就可以使用`width`或`height`来定义图片大小

> 通常情况下只需要在这2个属性里选择一个属性来定义大小就好了

**下面是用法演示和效果：**

```html
<h6>width 给图像设定宽度为100</h6>
<img src="https://yjf.vin/static/picture/1.jpg" width="100" />
```
<h6>width 给图像设定宽度为100</h6>
<img src="https://yjf.vin/static/picture/1.jpg" width="100" />

```html
<h6>height 给图像设定高度为100</h6>
<img src="https://yjf.vin/static/picture/1.jpg" height="100" />
```
<h6>height 给图像设定高度为100</h6>
<img src="https://yjf.vin/static/picture/1.jpg" height="100" />

#### - 那么还有一个属性叫`border`,这个是设置图像的边框粗细

**下面是用法演示和效果：**

```html
<h6>border 给图像设定边框为15</h6>
<img src="https://yjf.vin/static/picture/1.jpg" border="15" />
```
<h6>border 给图像设定边框为15</h6>
<img src="https://yjf.vin/static/picture/1.jpg" height="100" border="15" />

> 因为图像有点大，所以这个展示我加了个`height`属性

#### 图像标签属性注意点：

1. 图像标签可以拥有多个属性，必须写在标签名的后面
2. 属性之前不分前后顺序，标签名与属性、属性与属性之间均以空格分开
3. 属性采取键值对的格式，即key="value"的格式，属性="属性值"

### 2.路径

页面中的图片会非常多，通常我们会新建一个文件夹来存放这些图像文件（images）,这是再查找图像，就需要采用"路径"的方式来指定图像文件位置

##### 路径可分为：

1. 相对路劲

>`相对路劲：`以`引用文件所在位置`为参考基础，而建立出的目录路径。<br />这里简单来说，`图片相对于HTML页面的位置` 

|相对路径分类|符号|说明|
|:-------|:--|:--|
|同一级路径||图像文件位于HTML文件同一级 如<img src="yan.jpg"|
|下一级路径|/|图像文件位于HTML文件下一级 如<img src="images/yan.jpg"|
|上一级路径|../|图像文件位于HTML文件上一级 如<img src="../yan.jpg"|

> 可以[点我](https://www.bilibili.com/video/BV14J4114768?p=23&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)观看pink老师对相对路径的视频讲解

2. 绝对路劲

> `绝对路劲：`是指目录下的绝对位置，直接到达目标位置，通常是从盘符开始的路径
> - 例如：C:\Yan\images\yan.jpg或完整的网络地址”https://yan.vin/images/yan.jpg“

> 可以[点我](https://www.bilibili.com/video/BV14J4114768?p=25&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)观看pink老师对绝对路径的视频讲解

## 4.7超链接标签

在HTML标签中，`<a>`标签用于定义超链接，作用是从一个页面链接到另一个页面。可以简单理解为页面跳转

#### 1. 链接的语法格式：

```html
<a href="跳转目标" target="目标窗口的弹出方式">文本或图像</a>
```

单词anchor的缩写，意为：锚

|属性|说明|
:--|:--|
|href|用于指定链接目标的url地址，（必须属性）当为标签应用href属性时，它就具有了超链接的功能|
|target|用于指定链接页面的打开方式，其中_self为默认值，_blank为在新窗口中打开方式|

#### 演示：
```html
<h6>点击打开Yan的介绍</h6>
<a href="https://yjf.vin">Yan的介绍</a>
<h6>_self 当前窗口打开Yan的介绍</h6>
<a href="https://yjf.vin" target="_self">Yan的介绍</a>
<h6>_blank 新窗口打开Yan的介绍</h6>
<a href="https://yjf.vin" target="_blank">Yan的介绍</a>
```

**效果：**

<h6>点击打开Yan的介绍</h6>
<a href="https://yjf.vin">Yan的介绍</a>
<h6>_self 当前窗口打开Yan的介绍</h6>
<a href="https://yjf.vin" target="_self">Yan的介绍</a>
<h6>_blank 新窗口打开Yan的介绍</h6>
<a href="https://yjf.vin" target="_blank">Yan的介绍</a>

> 通过上面演示可以发现`target`属性是可以不加的，如果需要新窗口打开网页就加`target`

#### 2. 链接分类：

**1. 外部链接：**

例如：
```html
<a href="https://yjf.vin">Yan的介绍</a>
```

**2. 内部链接：**网站内部页面之间的互相链接，直接链接内部页面名称即可

例如：
```html
<a href="index.html">Yan的介绍</a>
```

**3. 空链接：**如果当时没有确定链接目标时，可以在href属性值里写#

例如：

```html
<a href="#">Yan的介绍</a>
```

**4. 下载链接：**如果href属性值里面的链接是一个文件或者压缩包，会下载这个文件

例如：
```html
<a href="yan.zip">Yan的介绍</a>
```

**5. 网页元素链接：**在网页中的各种网页元素，如文本、图像、表格、音频、视频等都可以添加超链接

例如：
```html
<a href="https://yjf.vin"><img src="https://yjf.vin/static/picture/1.jpg" /></a>
```

<a href="https://yjf.vin"><img src="https://yjf.vin/static/picture/1.jpg" width="100" /></a>

> 小白可能一时有点懵，其实这里就是用`img标签`当作文字，你点击图片，它就可以跳转到`Yan的介绍`里

**6. 锚点链接：**可以快速定位到页面中的某个位置

- 在链接文本的href属性中，设置属性值为`#名字`的形式,如:
```html
<a href="#yan">Yan的质料</a>
```

- 找到目标位置标签，里面添加一个id属性=刚才的名字,如:
```html
<h6 id="yan">Yan的介绍</h6>
```

# **5.HTML中的注释和特殊字符**

## 5.1注释

如果需要在HTML文档中添加一些便于阅读和理解但又不需要显示在页面中的注释文字，就需要使用注释标签

HTML中的注释以`<!--`开头，以`-->`结束

#### 语法格式：
```html
<!-- 要注释的内容 -->
```

> 在VSCode中，可以使用快捷键：`Ctrl`+`/`

## 5.2特殊字符

在HTML页面中，一些特殊的符号很难或者不方便直接使用，此时我们就可以使用下面的字符来替代

<img src="./images/YanCchen_2022-08-18_22-12-08.png" class="img" />

> 还有更多可以查看[这里](https://blog.csdn.net/u013778905/article/details/53177042)，或自行[百度](https://cn.bing.com/search?q=+html%E4%B8%AD%E7%9A%84%E7%89%B9%E6%AE%8A%E5%AD%97%E7%AC%A6)