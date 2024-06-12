# HTML标签（下）

# **1.表格标签**

1. 表格的主要用法
2. 表格的基本语法

## 1.1表格的主要作用

表格主要用于`显示`、`展示数据`，因为它可以让数据显示的非常的规整，可读性非常好。特别是后台展示数据的时候，能够熟练运用表格就显得很重要。一个清爽简约的表格能够把繁杂的数据表现得很有条理

> 表格不是用来布局页面的，而是用来`展示数据`的形式


<img src="./images/YanCchen_2022-08-19_09-56-58.png" class="img" />

## 1.2表格的基本语法

#### 语法格式：

```html
<table>
    <tr>
        <td>单元格内的文字</td>
        ···
    </tr>
    ···
</table>
```

1. `<table></table>`是用于定义表格的标签
2. `<tr></tr>`标签用于定义表格中的行，必须嵌套在`<table></table>`标签中
3. `<td></td>`用于定义表格中的单元格，必须嵌套在`<tr></tr>`标签中
4. 字母td指表格数据（table data）,即数据单元格的内容


<img src="./images/YanCchen_2022-08-19_10-21-00.png" class="img" />

#### 演示：

```html
<table>
        <tr><td>姓名</td>  <td>性别</td> <td>年龄</td></tr>
        <tr><td>刘德华</td>  <td>男</td> <td>56</td></tr>
        <tr><td>张学友</td>  <td>男</td> <td>58</td></tr>
        <tr><td>郭富城</td>  <td>男</td> <td>51</td></tr>
        <tr><td>黎明</td>  <td>男</td> <td>57</td></tr>
</table>
```

**效果：**

<table>
        <tr><td>姓名</td>  <td>性别</td> <td>年龄</td></tr>
        <tr><td>刘德华</td>  <td>男</td> <td>56</td></tr>
        <tr><td>张学友</td>  <td>男</td> <td>58</td></tr>
        <tr><td>郭富城</td>  <td>男</td> <td>51</td></tr>
        <tr><td>黎明</td>  <td>男</td> <td>57</td></tr>
</table>

## 1.3表头单元格标签

一般表头单元格位于表格的第一行或第一列，表头单元格里面的文本内容加粗居中显示

`<th>`标签表示HTML表格的标头部分(table head的缩写)

#### 语法格式：

```html
<table>
    <tr>
        <th>姓名</th>
        ···
    </tr>
    ···
</table>
```

<img src="./images/YanCchen_2022-08-19_10-34-33.png" class="img" />

#### 演示：

```html
<table>
        <tr><th>姓名</th>  <th>性别</th> <th>年龄</th></tr>
        <tr><td>刘德华</td>  <td>男</td> <td>56</td></tr>
        <tr><td>张学友</td>  <td>男</td> <td>58</td></tr>
        <tr><td>郭富城</td>  <td>男</td> <td>51</td></tr>
        <tr><td>黎明</td>  <td>男</td> <td>57</td></tr>
</table>
```

**效果：**

<table>
        <tr><th>姓名</th>  <th>性别</th> <th>年龄</th></tr>
        <tr><td>刘德华</td>  <td>男</td> <td>56</td></tr>
        <tr><td>张学友</td>  <td>男</td> <td>58</td></tr>
        <tr><td>郭富城</td>  <td>男</td> <td>51</td></tr>
        <tr><td>黎明</td>  <td>男</td> <td>57</td></tr>
</table>

## 1.4表格属性

> 表格标签这部分属性我们实际开发我们不常用，后面通过CSS来设置

目的有2个：

1. 记住这些英语单词，后面CSS会使用
2. 直观感受表格的外观形态

|属性名|属性值|描述|
|:-------|:--|:--|
|align|left、center、right|规定表格相对周围元素的对齐方式。|
|bgcolor	|颜色名字或颜色二进制代码	|规定表格的背景颜色。|
|border	|1或者其他" "	|规定表格单元是否拥有边框，默认为" "，表示没有边框。|
|cellpadding	|像素值	|规定单元边沿与其内容之间的空白，默认1像素。|
|cellspacing	|像素值	|规定单元格之间的空白，默认为2像素。|
|width	|像素值或百分比	|规定表格的宽度。|

> 还有更多可以查看[这里](https://blog.csdn.net/ofshitao/article/details/118876846)，或自行[百度](https://cn.bing.com/search?q=HTML%E8%A1%A8%E6%A0%BC%E5%B1%9E%E6%80%A7)

#### 演示：

```html
<!-- 这些属性要写到表格标签<table>里面去 -->
<table align="center" bgcolor="#efc3e1" border="1" cellpadding="20" cellspacing="0" width="500">
        <tr><th>姓名</th>  <th>性别</th> <th>年龄</th></tr>
        <tr><td>刘德华</td>  <td>男</td> <td>56</td></tr>
        <tr><td>张学友</td>  <td>男</td> <td>58</td></tr>
        <tr><td>郭富城</td>  <td>男</td> <td>51</td></tr>
        <tr><td>黎明</td>  <td>男</td> <td>57</td></tr>
</table>
```

> `表格属性`要写到表格标签`<table>`里面去

> 添加的代码属性解释：
> - align：居中显示
> - bgcolor：背景颜色改为粉色
> - border：边框像素设置成1
> - cellpadding：边框和文字的距离设置成20
> - cellspacing：单元格之间的距离设置成0
> - width：设置宽度为500

**效果：**

<img src="./images/YanCchen_2022-08-19_11-16-59.png" class="img" />

> 因为文档问题，无法正常展示，所以这里用图片展示。你可以创建个html文档查看最终效果

## 1.5表格结构标签

使用场景：因为表格可能很长，为了更好的表示表格的语义，可以将表格分割成`表格头部`和`表格主体`两大部分

在表格标签中，分别用：`<thead>标签` `表格的头部区域`、`<tbody>标签` `表格的主体区域`。这样可以更好的分清表格结构

1. `<thead></thead>`:用于定义表格的头部。`<thead>`内部必须拥有`<tr>`标签。一般位于第一行
2. `<tbody></tbody>`:用于定义表格的主题，主要用于放数据本体
3. 以上标签都是放在`<table></table>`标签中

#### 演示：
```html
<table>
        <thead>
            <tr><th>姓名</th>  <th>性别</th> <th>年龄</th></tr>
        </thead>
        <tbody>
        <tr><td>刘德华</td>  <td>男</td> <td>56</td></tr>
        <tr><td>张学友</td>  <td>男</td> <td>58</td></tr>
        <tr><td>郭富城</td>  <td>男</td> <td>51</td></tr>
        <tr><td>黎明</td>  <td>男</td> <td>57</td></tr>
        </tbody>
</table>
```

**效果：**

<table>
        <thead>
            <tr><th>姓名</th>  <th>性别</th> <th>年龄</th></tr>
        </thead>
        <tbody>
        <tr><td>刘德华</td>  <td>男</td> <td>56</td></tr>
        <tr><td>张学友</td>  <td>男</td> <td>58</td></tr>
        <tr><td>郭富城</td>  <td>男</td> <td>51</td></tr>
        <tr><td>黎明</td>  <td>男</td> <td>57</td></tr>
        </tbody>
</table>

> 可以[点我](https://www.bilibili.com/video/BV14J4114768?p=37&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)观看pink老师对表格结构标签的视频讲解

## 1.6合并单元格

特殊情况下，可以把多个单元格合并为一个单元格，这里理解最简单的合并单元格即可

1. 合并单元格方式
2. 目标单元格
3. 合并单元格的步骤

#### 合并单元格方式：

- 跨行合并：rowspan="合并单元格的个数"
- 跨列合并：colspan="合并单元格的个数"

<img src="./images/YanCchen_2022-08-19_11-48-33.png" class="img" />

#### 目标单元格：（写合并代码）

- 跨行：最上侧单元格为目标单元格，写合并代码
- 跨列：最左侧单元格为目标单元格，写合并代码

#### 合并单元格三部曲：

1. 先确定是跨行还是跨列合并
2. 找到目标单元格，写上合并方式=合并的单元格数量。比如：`<td colspan="2"></td>`
3. 删除多余的单元格

#### 演示：

```html
<table width="500" height="249" border="1" cellspacing="0">
        <tr>
            <td></td>
            <td colspan="2"></td>
        </tr>
        <tr>
            <td rowspan="2"></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
        </tr>
</table>
```

**效果：**

<img src="./images/YanCchen_2022-08-19_12-09-05.png" class="img" />

> 因为文档问题，无法正常展示，所以这里用图片展示。你可以创建个html文档查看最终效果

> 可以[点我](https://www.bilibili.com/video/BV14J4114768?p=38&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)观看pink老师对合并单元格的视频讲解

## 1.7表格总结

表格学习整体可以分为三大部分：

1. 表格的相关标签
2. 表格的相关属性
3. 合并单元格

> 可以[点我](https://www.bilibili.com/video/BV14J4114768?p=39&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)观看pink老师对表格总结的视频讲解

# **2.列表标签**

表格里用来显示数据的，那么`列表就是用来布局的`

列表最大的特点就是`整齐`、`整洁`、`有序`，它作为布局会更加自由和方便

根据使用情景不同，列表可以分为三大类：`无序列表`、`有序列表`和`自定义列表`

<img src="./images/YanCchen_2022-08-19_13-03-55.png" class="img" />

## 2.1无序列表

`<ul>`标签表示HTML页面中项目的无序列表，一般会以项目符号呈现列表项，而列表项使用`<li>`标签定义

#### 无序列表的基本语法格式：

```html
<ul>
    <li>列表1</li>
    <li>列表2</li>
    <li>列表3</li>
    ···
</ul>
```

1. 无序列表的各个列表项之间没有顺序级别之分，是并列的
2. `<ul></ul>`中只能嵌套`<li></li>`，直接在`<ul></ul>`标签中输入其他标签或文字的做法是不被允许的
3. `<li>`与`</li>`之间相当于一个容器，可以容纳所有元素
4. 无序列表会带有自己的样式属性，但在实际使用时，我们会使用CSS在设置

#### 演示：

```html
<h4>你喜欢的食物？</h4>
<ul>
    <li>榴莲</li>
    <li>臭豆腐</li>
    <li>鲱鱼罐头</li>
</ul>
```

**效果：**

<h4>你喜欢的食物？</h4>
<ul>
    <li>榴莲</li>
    <li>臭豆腐</li>
    <li>鲱鱼罐头</li>
</ul>

## 2.2有序列表

有序列表即为有排列顺序的列表，其各个列表项会按照一定的顺序排列定义

在HTML标签中，`<ol>`标签用于定义有序列表，列表排序以数字来显示，并且使用`<li>`标签来定义列表项

#### 有序列表的基本语法格式：

```html
<ol>
    <li>列表项1</li>
    <li>列表项2</li>
    <li>列表项3</li>
    ···
</ol>
```

1. `<ol></ol>`中只能嵌套`<li></li>`，直接在`<ol></ol>`标签中输入其他标签或文字的做法是不被允许的
2. `<li>`与`</li>`之间相当于一个容器，可以容纳所有元素
3. 有序列表会带有自己的样式属性，但在实际使用时，我们会使用CSS在设置

#### 演示：

```html
<h4>你喜欢的食物？</h4>
<ol>
    <li>榴莲</li>
    <li>臭豆腐</li>
    <li>鲱鱼罐头</li>
</ol>
```

**效果：**

<h4>你喜欢的食物？</h4>
<ol>
    <li>榴莲</li>
    <li>臭豆腐</li>
    <li>鲱鱼罐头</li>
</ol>

## 2.3自定义列表

自定义列表的使用场景：
- 自定义列表常用于对术语或名词进行解释和描述，定义列表的列表项前没有任何项目符号

<img src="./images/YanCchen_2022-08-19_13-40-13.png" class="img" />

在HTML标签中，`<dl>`标签用于定义自定义列表（或定义列表），该标签会与`<dt>`（定义项目/名字）和`<dd>`（描述每一个项目/名字）一起使用

#### 自定义列表的基本语法格式：

```html
<dl>
    <dt>名称1</dt>
    <dd>名词1解释1</dd>
    <dd>名词1解释2</dd>
</dl>
```

1. `<dl></dl>`里面只能包含`<dt>`和`<dd>`
2. `<dt>`和`<dd>`个数没有限制，经常是一个`<dt>`对应多个`<dd>`

#### 演示：

```html
<dl>
    <dt>关注我们</dt>
    <dd>Github</dd>
    <dd>官方微信</dd>
    <dd>哔哩哔哩</dd>
</dl>
```

**效果：**

<dl>
    <dt>关注我们</dt>
    <dd>Github</dd>
    <dd>官方微信</dd>
    <dd>哔哩哔哩</dd>
</dl>

## 2.4列表总结

|标签名|定义|说明|
|:-------|:--|:--|
|`<ul></ul>`|无序列表|里面只能包含`<li>` 没有顺序，使用较多。`<li>`里面可以包含任何标签|
|`<ol></ol>`|有序列表|里面只能包含`<li>` 有顺序，使用相对较少。`<li>`里面可以包含任何标签|
|`<dl></dl>`|自定义列表|里面只能包含`<dt>`和`<dd>`。`<dt>`和`<dd>`里面可以放任何标签|

> 可以[点我](https://www.bilibili.com/video/BV14J4114768?p=43&spm_id_from=pageDriver&vd_source=5ce077ad2b5b1249c5cc46b02b39814a)观看pink老师对列表总结的视频讲解

# **3.表单标签**

现实中的表单，我们去银行办理信用卡填写的单子

<img src="./images/YanCchen_2022-08-19_14-05-02.png" class="img" height="400"/>

网页中的表单展示


<img src="./images/YanCchen_2022-08-19_14-07-30.png" class="img" height="400"/>

## 3.1为什么需要表单

使用表单目的是为了`收集用户信息`

在我们网页中，我们也需要跟用户进行交互，收集用户质料，此时就需要表单

## 3.2表单的组成

在HTML中，一个完整的表单通常由`表单域`、`表单控件（也称为表单元素）`和`提示信息`3个部分构成


<img src="./images/YanCchen_2022-08-19_14-16-33.png" class="img"/>

## 3.3表单域

`表单域`是一个`包含表单元素的区域`

在HTML标签中，`<form>`标签用于定义表单域，以实现用户信息的收集和传递

`<form>会把它范围内的表单元素信息提交给服务器`

#### 语法格式：
```html
<form action="url地址" method="提交方式" name="表单域名称">
    各种表单元素控件
</form>
```

**常用属性**

|属性|属性值|说明|
|:-------|:--|:--|
|action|url地址|用于指定接收并处理表单数据的服务器程序的url地址|
|method|get/post|用于设置表单数据的提交方式，有两种方式get或post|
|name|名称|用于指定表单的名称，方便区分同一个页面中的多个表单域|

#### 演示：

```html
<form action="yan.php" method="post" name="Yan">
    各种表单元素控件
</form>
```

## 3.4表单控件(表单元素)

在表单域中可以定义各种表单元素，这些表单元素就是允许用户在表单中输入或者选择的内容控件

接下来先讲解：

1. input输入表单元素
2. select下拉表单元素
3. textarea文本域元素

> 内容较多，点击以下导航
> - [3.4.1&lt;input&gt;表单元素](/HTML基础/DIERTIAN?id=_341ltinputgt表单元素)
> - [3.4.2&lt;label&gt;标签](/HTML基础/DIERTIAN?id=_342ltlabelgt标签)
> - [3.4.3&lt;select&gt;表单元素](/HTML基础/DIERTIAN?id=_343ltselectgt表单元素)
> - [3.4.4&lt;textarea&gt;表单元素](/HTML基础/DIERTIAN?id=_344lttextareagt表单元素)

### 3.4.1&lt;input&gt;表单元素

在英文单词中，input是输入的意思，而在表单元素中`<input>标签用于收集用户信息`

在`<input>`标签中，包含一个`type`属性，根据不同的`type`属性值，输入字段拥有很多种形式（可以是文本字段、复选框、掩码后的文本控件、单选按钮、按钮等）

#### 语法格式：
```html
<input type="属性值" />
```

1. `<input>`标签为单标签
2. type属性设置不同的属性值用来指定不同的控件类型

`type`属性的属性值及描述如下：

<img src="./images/YanCchen_2022-08-19_14-58-23.png" class="img" height="400"/>

> [点击我](https://cn.bing.com/search?q=input%E6%A0%87%E7%AD%BE%E7%9A%84type%E5%B1%9E%E6%80%A7%E6%9C%89%E5%93%AA%E4%BA%9B)百度搜索更多type属性的属性值

#### 演示：

```html
<form action="yan.php" method="post" name="Yan">
    <!-- file 上传文件 -->
    上传头像：<input type="file">
    <br>
    <!-- text 文本框 用户可以在里面输入任何文字 -->
    用户名：<input type="text">
    <br>
    <!-- password 密码框 用户看不见输入的密码 -->
    密码：<input type="password">
    <br>
    <!-- radio 单选按钮 可以实现多选一 -->
    性别：<input type="radio">男<input type="radio">女<input type="radio">人妖
    <br>
    <!-- checkbox 复选框 可以实现多选 -->
    爱好：<input type="checkbox">吃饭<input type="checkbox">睡觉<input type="checkbox">摸鱼
    <br>
    <!-- submit 提交按钮 -->
    <input type="submit">
    <!-- reset 重置按钮 -->
    <input type="reset">
</form>
```

**效果：**

<form action="yan.php" method="post" name="Yan">
    <!-- file 上传文件 -->
    上传头像：<input type="file">
    <br>
    <!-- text 文本框 用户可以在里面输入任何文字 -->
    用户名：<input type="text">
    <br>
    <!-- password 密码框 用户看不见输入的密码 -->
    密码：<input type="password">
    <br>
    <!-- radio 单选按钮 可以实现多选一 -->
    性别：<input type="radio">男<input type="radio">女<input type="radio">人妖
    <br>
    <!-- checkbox 复选框 可以实现多选 -->
    爱好：<input type="checkbox">吃饭<input type="checkbox">睡觉<input type="checkbox">摸鱼
    <br>
    <!-- submit 提交按钮 -->
    <input type="submit">
    <!-- reset 重置按钮 -->
    <input type="reset">
</form>





**除type属性外，`<input>`标签还有其他很多属性，其常用属性如下：**

<img src="./images/YanCchen_2022-08-19_15-21-00.png" class="img"/>

1. name和value是每个表单元素都有的属性值，主要给后台人员使用
2. name表单元素的名字,要求`单选按钮和复选框要有相同的name值`
3. `checked属性主要针对于单选按钮和复选框`，主要作用一打开页面，就可以默认选中某个表单元素
4. maxlength是用户可以在表单元素输入的最大字符数，一般较少使用

#### `name`、`value`的属性演示：

```html
<form action="yan.php" method="post" name="Yan">
    <!-- file 上传文件 -->
    上传头像：<input type="file">
    <br>
    <!-- text 文本框 用户可以在里面输入任何文字 -->
    用户名：<input type="text" name="username" value="你叫啥？">
    <br>
    <!-- password 密码框 用户看不见输入的密码 -->
    密码：<input type="password" name="pwd">
    <br>
    <!-- radio 单选按钮 可以实现多选一 -->
    <!-- name 是表单元素名字 这里性别单选框按钮必须有相同的名字name 才可以实现多选一 -->
    性别：<input type="radio" name="sex" value="男">男<input type="radio" name="sex" value="女">女<input type="radio" name="sex" value="人妖">人妖
    <br>
    <!-- checkbox 复选框 可以实现多选 -->
    爱好：<input type="checkbox" name="hobby" value="吃饭">吃饭<input type="checkbox" name="hobby" value="睡觉">睡觉<input type="checkbox" name="hobby" value="摸鱼">摸鱼
    <br>
    <!-- submit 提交按钮 -->
    <input type="submit" value="点我提交">
    <!-- reset 重置按钮 -->
    <input type="reset" value="重新填写">
</form>
```

**效果：**

<form action="yan.php" method="post" name="Yan">
    <!-- file 上传文件 -->
    上传头像：<input type="file">
    <br>
    <!-- text 文本框 用户可以在里面输入任何文字 -->
    用户名：<input type="text" name="username" value="你叫啥？">
    <br>
    <!-- password 密码框 用户看不见输入的密码 -->
    密码：<input type="password" name="pwd">
    <br>
    <!-- radio 单选按钮 可以实现多选一 -->
    <!-- name 是表单元素名字 这里性别单选框按钮必须有相同的名字name 才可以实现多选一 -->
    性别：<input type="radio" name="sex" value="男">男<input type="radio" name="sex" value="女">女<input type="radio" name="sex" value="人妖">人妖
    <br>
    <!-- checkbox 复选框 可以实现多选 -->
    爱好：<input type="checkbox" name="hobby" value="吃饭">吃饭<input type="checkbox" name="hobby" value="睡觉">睡觉<input type="checkbox" name="hobby" value="摸鱼">摸鱼
    <br>
    <!-- submit 提交按钮 -->
    <input type="submit" value="点我提交">
    <!-- reset 重置按钮 -->
    <input type="reset" value="重新填写">
</form>

#### `checked`和`maxlength`的属性演示：

```html
<form action="yan.php" method="post" name="Yan">
    <!-- file 上传文件 -->
    上传头像：<input type="file">
    <br>
    <!-- text 文本框 用户可以在里面输入任何文字 -->
    <!-- maxlength 正整数 设置最长输入6个字 -->
    用户名：<input type="text" name="username" value="你叫啥？" maxlength="6">
    <br>
    <!-- password 密码框 用户看不见输入的密码 -->
    密码：<input type="password" name="pwd">
    <br>
    <!-- radio 单选按钮 可以实现多选一 -->
    <!-- name 是表单元素名字 这里性别单选框按钮必须有相同的名字name 才可以实现多选一 -->
    <!-- 单选按钮和复选框可以设置checked 属性，当页面打开的时候就可以默认选中这个按钮 -->
    性别：<input type="radio" name="sex" value="男">男<input type="radio" name="sex" value="女">女<input type="radio" name="sex" value="人妖" checked="checked">人妖
    <br>
    <!-- checkbox 复选框 可以实现多选 -->
    爱好：<input type="checkbox" name="hobby" value="吃饭">吃饭<input type="checkbox" name="hobby" value="睡觉">睡觉<input type="checkbox" name="hobby" value="摸鱼" checked="checked">摸鱼
    <br>
    <!-- submit 提交按钮 -->
    <input type="submit" value="点我提交">
    <!-- reset 重置按钮 -->
    <input type="reset" value="重新填写">
</form>
```

**效果：**

<form action="yan.php" method="post" name="Yan">
    <!-- file 上传文件 -->
    上传头像：<input type="file">
    <br>
    <!-- text 文本框 用户可以在里面输入任何文字 -->
    <!-- maxlength 正整数 设置最长输入6个字 -->
    用户名：<input type="text" name="username" value="你叫啥？" maxlength="6">
    <br>
    <!-- password 密码框 用户看不见输入的密码 -->
    密码：<input type="password" name="pwd">
    <br>
    <!-- radio 单选按钮 可以实现多选一 -->
    <!-- name 是表单元素名字 这里性别单选框按钮必须有相同的名字name 才可以实现多选一 -->
    <!-- 单选按钮和复选框可以设置checked 属性，当页面打开的时候就可以默认选中这个按钮 -->
    性别：<input type="radio" name="sex" value="男">男<input type="radio" name="sex" value="女">女<input type="radio" name="sex" value="人妖" checked="checked">人妖
    <br>
    <!-- checkbox 复选框 可以实现多选 -->
    爱好：<input type="checkbox" name="hobby" value="吃饭">吃饭<input type="checkbox" name="hobby" value="睡觉">睡觉<input type="checkbox" name="hobby" value="摸鱼" checked="checked">摸鱼
    <br>
    <!-- submit 提交按钮 -->
    <input type="submit" value="点我提交">
    <!-- reset 重置按钮 -->
    <input type="reset" value="重新填写">
</form>

### 3.4.2&lt;label&gt;标签

`<label>`标签为input元素定义标注(`标签`)

`<label>`标签用于绑定一个表单元素，当点击`<label>`标签内的文本时，浏览器就会自动将焦点（光标）转到或者选择对应的表单元元素上，用来增加用户体验

#### 语法格式：

```html
<label for="sex">男</label>
<input type="radio" name="sex" id="sex" />
```

> 核心：`<label>`标签的`for属性`应当与相关元素的`id属性相同`

#### 演示：

```html
<label for="用户名">用户名：</label><input type="text" id="用户名">
<br>
<label for="密码">密码</label><input type="password" id="密码">
<br>
<input type="radio" name="sex" id="男"> <label for="男">男</label>
<input type="radio" name="sex" id="女"> <label for="女">女</label>
<input type="radio" name="sex" id="人妖"> <label for="人妖">人妖</label>
```

**效果：**

<label for="用户名">用户名：</label><input type="text" id="用户名">
<br>
<label for="密码">密码</label><input type="password" id="密码">
<br>
<input type="radio" name="sex" id="男"> <label for="男">男</label>
<input type="radio" name="sex" id="女"> <label for="女">女</label>
<input type="radio" name="sex" id="人妖"> <label for="人妖">人妖</label>

### 3.4.3&lt;select&gt;表单元素

使用场景：在页面中，如果有多个选项让用户选择，并且想要节约页面空间时，我们可以使用`<select>`标签控件定义`下拉列表`

#### 语法格式：

```html
<select>
    <option>选项1</option>
    <option>选项2</option>
    <option>选项3</option>
    ···
</select>
```

1. `<select>`中至少包含一对`<option>`
2. 在`<select>`中定义selected="selected"时，当前项为默认选中项

#### 演示：

```html
你是哪里人？
<select>
    <option>地球人</option>
    <option>火星人</option>
    <!-- 使用selected属性，打开页面默认选中 -->
    <option selected="selected">水星人</option>
    <option>木星人</option>
    <option>金星人</option>
</select>
```

**效果：**

你是哪里人？
<select>
    <option>地球人</option>
    <option>火星人</option>
    <!-- 使用selected属性，打开页面默认选中 -->
    <option selected="selected">水星人</option>
    <option>木星人</option>
    <option>金星人</option>
</select>

### 3.4.4&lt;textarea&gt;表单元素

使用场景：当用户输入内容较多的情况下，我们就不能使用文本框表单了，此时我们可以使用`textarea`标签

在表单元素中，`textarea`标签是用于定义多行文本输入的控件

使用多行文本输入控件，可以输入更多的文字，该控件常见于留言板，评论

#### 语法格式：

```html
<textarea rows="3" cols="20">
    文本内容
</textarea>
```

1. 通过`textarea`标签可以轻松地创建多行文本输入框
2. cols="每行中的字符数"，rows="显示的行数"，我们在实际开发中不会使用，都是用CSS来改变大小

#### 演示：

```html
今天吃的什么：<br>
<textarea rows="3" cols="20">我吃的啥不重要，重要的是你怎么又摸鱼了</textarea>
```

**效果：**

今天吃的什么：<br>
<textarea rows="3" cols="20">我吃的啥不重要，重要的是你怎么又摸鱼了</textarea>