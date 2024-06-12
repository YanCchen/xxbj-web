## CSS引入方式

css引入方式共有一下3种

```html
外部引入：<link rel="stylesheet" type="text/css" href="文件路径"/>
内部引入:<style type="text/css"></style>
行内引入：<div style="color:red"></div>
```

## 字体样式

```css
font-family 字体类型                             font-size 字体大小
语法：font-family:字体1，字体2，字体3              语法：font-size：取值
可选值：Arial "Times new Roman" "微软雅黑"        可选值的单位：px em rem %

font-weight 字体粗细                            font-style 字体风格
语法:font-weight：取值                          语法:font-style：取值
可选值：normal 正常   lighter 较细               可选值：normal 正常   italic 斜体
       bolder 很粗   bold 较粗                          oblique 斜体       
```

## CSS注释

```html
语法：/* 注释内容 */
```

## 文本样式

```css
text-decoration 文本修饰                   text-indent 首行缩进 
语法：text-decoration：取值                语法：text-indent：像素值 
可选值： none 去除所有效果                 
        overline  顶划线                   line-height 行高 
        underline 下划线                   语法:line-height：像素值
        line-through 中划线
        
text-align  水平对齐
语法：text-align：取值
可选值：left 左对齐   center 居中对齐 
       right 右对齐

```

## 间距

```css
letter-spacing 字间距 语法：letter-spacing：像素值
word-spacing 词间距   语法：word-spacing：像素值
```

## 边框样式

```css
border-width  边框的宽度   border-height 边框的高度   border-color 边框的颜色
border-style  边框的样式
可选值：none 无样式   dashed 虚线   solid 实线
border的简写样式 语法：border：宽度 颜色 样式 
```

## 边框的局部样式

```css
border-top 上边框   border-bottom 下边框   border-left 左边框   border-right 右边框
边框局部简写语法：border-top：1px solid red
```

## 列表样式

```css
list-style-type 列表项目符号     语法：list-style-type：取值
可选值：lower-roman 小罗马数字    upper-roman 大写罗马数字       
       lower-alpha 小写英语      upper-alpha 大写英语       
       decimal     阿拉伯数字    disc  实心圆       
       circle      空心圆        square 正方形   
```

## 表格样式

```CSS
caption-side 表格标题位置   语法：caption-side：取值
可选值：top 标题在顶部   bottom 标题在底部

border-collapse 表格边框合并 语法： border-collapse：取值
可选值：separate 边框分开，有空隙
       collapse 边框合并，无空隙

border-spacing 表格边框间距  语法：border-spacing：像素值
```

## 图片样式

```css
text-align 图片对齐   语法：text-align：取值
可选值：left 左对齐   right 右对齐   center 居中对齐

vertical-align 垂直对齐   语法：vertical-align：取值
可选值：top 顶部对齐   middle 中部对齐
       baseline 基线对齐   bottom 底部对齐

图片大小：width 宽度   height 高度
图片边框：border：1px solid red
```

## 文字环绕

```css
float 文字环绕   语法：float：取值 可选值:left 元素向左浮动   right：元素向右浮动
```

## 背景样式

```css
background-color 背景颜色   语法：background-color：颜色值
background-image 背景图片   语法：background-image：url（图片路径）

background-repeat 图片背景重复 语法：background-repeat：取值
可选值：repeat 在水平和垂直方向上同时平铺   repeat-x 只在水平方向（x轴）上平铺
       repeat-y 只在垂直方向（y轴）上平铺  no-repeat 不平铺

background-position 图片背景位置   语法：background-position：像素值/关键字
background-attachment 背景图片固定 语法：background-attachment：取值
可选值：sroll 随元素一起滚动   fixed 固定不动
```

## 超链接伪类

```
a:link 定义a元素位访问的样式            a:visited 定义a元素访问后的样式
a：hover 定义a元素鼠标经过时的样式       a:active 定义鼠标单击激活时的样式
```

## 鼠标样式

```css
cursor 鼠标样式   语法：cursor：取值 可选值：default pointer text wait 
自定义鼠标样式 语法：cursor：url（图片地址），属性值
鼠标图片后缀一般都是“.cur”，属性值一般都是default pointer text
```

## 浮动布局

```css
float 浮动   语法：float：取值   可选值:left 元素向左浮动   right 元素向右浮动
```

## 清除浮动

```css
clear 清除浮动   语法：clear：取值   可选值：left 清除左浮动  right 清除右浮动 both 同时清除左右浮动
```

## 定位布局

```css
position 开启定位 语法：position：取值 
可选值:fixed 固定定位 relative 相对定位 absolute 绝对定位  static 静态定位
4中定位可选值：top：像素值 bottom：像素值 left：像素值 right：像素值
```

## 显示模式元素转换

```css
display：block 转换为块级元素     display：inline 转换为行内元素   display：inline-block 转换为行内块元素
```

## ：focus 伪类选择器

```css
：focus 伪类块级元素 语法：input：focus{background-color：red} 用于选取活动焦点的表单元素，一般都在input类
```

## 元素的显示与隐藏

```css
display：none 隐藏元素  display：block 显示元素  visibility：visible元素可视   visibility：hidden 元素隐藏
display不保留位置，visibility保留位置
```

## 新增的属性选择器

```css
input[value] 必须是input同时具有value这个属性，选择这个属性
input[type=text]选择input里的type的值为text
div[class^=icon]选择首先是div具有class属性而且必须是icon开头的
```

## 伪类选择器

```css
:first-child 选择第一个子元素      :last-child 选择最后一个子元素    :nth-child(n)选择第n个子元素
:first-of-type 指定类型的第一个    :last-of-type 指定类型的最后一个  :nth-of-type(n)指定类型的第n个

:nth-child()可以是数字也可以是公式也可以是关键字
关键字：even 偶数   odd 奇数
公式：2n 偶数  2n+1 奇数 5n:5 10 15...  n+5 从第5个开始包含第5个到最后
区别：
1.nth-child 对父元素里面所有的孩子排序选择(序号固定)先找到第n个孩子，后面再看看是否匹配。
2.nth-of-type 对父元素里面指定的子元素进行排序，先去匹配然后再根据找到第n个孩子。
```

## 伪元素选择器

```css
::before 在元素内部前面插入内容                                           ::after 在元素内部后面插入内容
before和after创建一个元素，单是属于行内元素，在文档树中找不到所以称为伪元素。
语法:element::before{content:""}before和after必须要有content属性	
```

## 计算盒子宽度

```less
width:cala(100%-80px)可使用 + - * /
```

## snipaste小工具

```css
按F1可截图，测量大小，设置箭头，书写文字等。
按F3可在桌面置顶显示
按Esc可取消图片显示
点击图片alt可取色(按shift可切换取色模式)
```

## CSS常用代码

```css
text-align:center 文本居中对齐							text-decoration:none 去除所有划线效果
text-indent:20px  所有段落首行缩进20像素					  background:rgba(0,0,0,0.5)背景颜色半透明
outline:none 去除input输入框的轮廓线						  resize:none 防止textarea拖拽
*{padding:0 margin:0} 去除所有默认样式					   border-radius：数值(px或%) 圆角
list-style-type:none 去除项目符号							opacity：0.5 半透明
border:none 去除input边框                                scroll-behavior: smooth; 平滑滚动
```

