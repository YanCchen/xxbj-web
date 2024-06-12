## meta标签简介

meta标签一般用于定义页面的特殊信息，比如页面关键字、页面描述等。

在HTML中meta中有2个重要的属性：name和http-equiv

```html
(1) name 属性取值:

keywords 网页关键字
description 网页的描述
author 网页的作者
copyright 版权信息

(2)http-equiv 属性作用
<meta charet="uft-8"/> 定义网页所使用的编码
<meta http-equiv="refresh" content="5":url="网址" 定义网页自动刷新跳转
```

##  HTML注释语法

```html
语法: <!--注释内容-->
```

## 文本标签

```html
标题标签 h1~h6
水平线标签 hr
上标标签 sup
下划线标签 ins、u
段落标签 p
加粗标签 strong、b
下标标签 sub
大字号标签 big
换行标签 br
斜体标签 i、em
删除线标签 del、s
小子号标签 small
```

## 特殊符号

```html
&quot 双引号
&lsquo 左单引号
&rsquo 右单引号
&times 乘号
&divide 除号
&dt 大于号
&lt  小于号
&copy 版权
&reg 注册商标
&trade 商标
&deg 度
```

## 列表简介

在HTML中列表共分为3种：有序列表、无序列表、定义列表

```html
1.有序列表：ol li
      ol的type属性取值：1 a A i l
2.无序列表：ul li
      ul的type属性取值：disc cirde square
3.定义列表：dl dt dd
   dl表示定义列表   dt表示标题   dd表示描述
```

## 表格table标签

```html
table   表格标签
tr 行标签     
th 表头标签   
caption 表格标题  
td 单元格标签 
1.rowspan 表格合并行（所谓合并行指的是将纵向的N个单元格合并）
语法：<td rowspan="跨域的行数"></td>
2.colspan 表格合并列（所谓合并列指的是将横向的N个单元格合并）
语法：<td colspan="跨域的列数"></td>
```

## 图片 img

```html
<img src="图片路径" alt="图片描述" title="图片标题" >
```

## 超链接   a标签

```html
<a href="链接地址" target="打开方式">文本或图片</a>
target属性取值：
_self   在原来的窗口打开链接(默认值)
_blank  在新窗口打开链接
_parent 在父窗口打开链接
_top    在顶层窗口打开链接
```

## 表单 form标签

```html
form属性：
name 表单名称
method 提交方式
action 提交地址
target 打开方式
name的值：自定义
method的值：get/post
action的值：url地址
```

## 新增的语义化标签  

```html
header  头部标签                                  aside   侧边栏标签
nav      导航标签                                   footer  底部标签
actide  内容标签                                    main    文档主要内容
progress  进度条                                    meter   度量器
fieldset  绘制表单边框                             legend定义fieldset的标题
```

## input表单新增的type属性

```html
<input type="text" />  单行文本框       <input type="password" /> 密码文本框 
<input type="radio" /> 单选框             <input type="checkbox" /> 多选框
<input type="button" /> 按钮              <input type="file" /> 上传文件
<input type="image" /> 图片按钮        <input type="reset" /> 重置按钮
<input type="submit" /> 提交按钮       <input type="textare" /> 多行文本框
<input type="email" /> 输入邮箱格式   <input type="url" /> url网址
<input type="time" /> 时间                 <input type="date" /> 日期
<input type="month" /> 月                 <input type="week" /> 周
<input type="number" /> 数字            <input type="tel" /> 手机号
<input type="search" /> 搜索框          <input type="color" /> 颜色菜单
```

## input表单新增的其他属性

```html
value      自定义文本内容
size 设置单行文本的长度
requlred  表单内容不能为空
placeholder 表单提示信息
autofocus  自动获得指定焦点
maxlength 设置最多输入字数
multiple  多选文件提交
pattern 行内正则表达式
autocomplete  值为off/on 保存用户输入过的值然后显示
```

## input表单新增的元素（datalist标签）

```html
<form action="" method="post">
    <input type="text" list="inputs"/>
    <datalist id="inputs">
        <option value ="" label=""></option>
        <option value ="" label=""></option>
    </datalist>
</form>

重点
1：option标签中创建选项值：value：具体的值，label：提示信息（辅助值）
2：input标签里的list属性的值为datalist标签里的id值
3：option可以是单标签也可以是双标签
4：如果input输入框的type类型是url，那么value的值必须添加http://

```

## audio音频标签

```html
属性：
src：播放的音频文件路径                 controls：音频播放器的控制面板
autoplay：自动播放                          loop：循环播放
语法：<audio src="播放的音频文件路径 " controls  autoplay  loop"></audio> 

```

## video 视频标签

```html
属性：
src：播放的音频文件路径                 controls：音频播放器的控制面板
autoplay：自动播放                          loop：循环播放
height：播放窗口高度                       width：播放窗口高度
poster：当视频还没有完全下载，或者用户还没有点击播放的默认显示的封面，默认显示当前视频的第一帧画面图。
typy：视频文件格式
代码示范：
<video controls >
<source  src="播放的音频文件路径 " poster =”视频默认显示的图片路径” typy=“video/mp4”>
对不起，您的浏览器不支持当前的视频播放
</video>
重点：
1：当设置宽高的时候，一般情况下只会设置宽度或者高度，让其自动的等比缩放，如果同时设置的宽度和高度，那么视频并不会真正的调整到设置的宽高，除非设置的值刚好是等比例。
2：source的使用，因为不同的浏览器支持的视频格式不一样，所以可以准备多个格式的视频文件，让浏览器自动选择。

```
