
<hong>HTML5</hong> 的新增特性主要是针对于以前的不足，增加了一些<hong>新的标签</hong>、<hong>新的表单</hong>和<hong>新的表单属性</hong>等<br>
这些新特性都有兼容性问题，基本是 IE9+ 以上版本的浏览器才支持，如果不考虑兼容性问题，可以大量使用这<br>
些新特性

声明：

新特性增加了很多，但是我们专注于开发常用的新特性

## 1.1 HTML5新增的语义化标签

以前布局，我们基本用 div 来做。div 对于搜索引擎来说，是没有语义的

```html
<div class=“header”> </div>
<div class=“nav”> </div>
<div class=“content”> </div>
<div class=“footer”> </div>
```

现在我们用这些更有语义化的标签来写网页会更好

- &lt;header>：头部标签
- &lt;nav>：导航标签
- &lt;article>：内容标签
- &lt;section>：定义文档某个区域
- &lt;aside>：侧边栏标签
- &lt;footer>：尾部标签

<img src="./images/YanCchen_2022-09-03_15-42-05.png" class="img" height="300" />

!> <hongcu>注意：</hongcu><br>
● 这种语义化标准主要是针对<hong>搜索引擎</hong>的<br>
● 这些新标签页面中可以使用<hong>多次</hong><br>
● 在 IE9 中，需要把这些元素转换为<hong>块级元素</hong><br>
● 其实，我们移动端更喜欢使用这些标签<br>
● HTML5 还增加了很多其他标签，我们后面再慢慢学

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=275&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=150.5)可以观看pink老师的讲解

## 1.2 HTML5新增的多媒体标签

新增的多媒体标签主要包含两个：

<hong>1. 音频：&lt;audio></hong><br>
<hong>2. 视频：&lt;video></hong>

使用它们可以很方便的在页面中嵌入音频和视频，而不再去使用 flash 和其他浏览器插件

> HTML5 在不使用插件的情况下，也可以原生的支持视频格式文件的播放，当然，支持的格式是有限的

### 1. 视频&lt;video>

当前 &lt;video> 元素支持三种视频格式： 尽量使用 mp4格式

<img src="./images/YanCchen_2022-09-03_16-06-43.png" class="img" height="300" />

#### 语法：

```html
<video src="文件地址" controls="controls"></video>
```
```html
<video controls="controls" width="300">
 <source src="move.ogg" type="video/ogg" >
 <source src="move.mp4" type="video/mp4" >
 您的浏览器暂不支持 video 标签播放视频
 </video >
```

####  常见属性

<img src="./images/YanCchen_2022-09-03_16-09-29.png" class="img" height="400" />

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=276&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 2. 音频&lt;audio>

当前 &lt;audio> 元素支持三种音频格式：

<img src="./images/YanCchen_2022-09-03_16-11-33.png" class="img" />

#### 语法：

```html
<audio src="文件地址" controls="controls"></audio>
```
```html
< audio controls="controls" >
 <source src="happy.mp3" type="audio/mpeg" >
 <source src="happy.ogg" type="audio/ogg" >
 您的浏览器暂不支持 audio 标签
 </audio>
```

####  常见属性

<img src="./images/YanCchen_2022-09-03_16-13-01.png" class="img" />

- 谷歌浏览器把音频和视频自动播放禁止了

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=277&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解

### 3. 多媒体标签总结

- 音频标签和视频标签使用方式基本一致
- 浏览器支持情况不同
- 谷歌浏览器把音频和视频自动播放禁止了
- 我们可以给视频标签添加 muted 属性来静音播放视频，音频不可以（可以通过JavaScript解决）
- 视频标签是重点，我们经常设置自动播放，不使用 controls 控件，循环和设置大小属性

## 1.3 HTML5新增的input类型

<img src="./images/YanCchen_2022-09-03_16-35-13.png" class="img" />

- 重点记住： number tel search 这三个

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=278&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a&t=3.0)可以观看pink老师的讲解

## 1.4 HTML5新增的表单属性

<img src="./images/YanCchen_2022-09-03_16-47-39.png" class="img" />

<hongcu>可以通过以下设置方式修改placeholder里面的字体颜色：</hongcu>

```css
input::placeholder {
    color: pink;
 }
```

> 点击[这里](https://www.bilibili.com/video/BV14J4114768?p=279&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)可以观看pink老师的讲解