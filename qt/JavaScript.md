## JavaScript的引入方式

```html
行内引入：<input type="button" onclick="alert()">
内部引入：<script>//执行语句</script>
外部引入：<script src="文件路径"></script>
```
## javaScript注释
```javascript
//单行注释    /*多行注释*/
```
## javaScript输出语句
```html
alert()弹出警示框     console.log()控制台打印输出信息
promet()弹出输入框，用户可以输入
```
## 变量
```html
var a=1 声明变量名为a并赋值为1
```
## 数据类型
```html
Number 数字型     String 字符串   Boolean 布尔值
underfinded 未定义  Null 空值    Object 对象
数据类型共有以上六种数据类型,基本数据类型除object,其余全是基本数据类型变量的数据类型是只有程序在运行过程中根据等号右边的值来确定的。
```

## 判断数据类型
```html
isNaN()用来判断一个变量是否为非数字类型返回true表示不是数字型。
```
## 获取数据类型
```html
typeof 语法:console.log(typeof 变量名)
```
## 数据类型转换
```html
使用表单prompt获取过来的数据默认是字符串类型的此时就不能直接简单地进行加法运算需要转换变量的数据类型，通俗来说就是把一种数据类型的变量转换成另一种数据类型。
数字型转换为字符串类型
语法(1):变量.toString()
例:var num=10      var str=num.toString()
语法(2):String(变量)
例:var num=10      var str=string(num)
语法(3):和字符串拼接的结果都是字符串(隐式转换)
```
## 转换为数字型
```html
语法(1):parseInt(变量) 转换为数字型得到的是整数
语法(2):parseFloat(变量) 转化为数字型得到的是小数浮点数
语法(3):Number(变量) 强制转换为数字型
```
## 转换为布尔型
```html
语法:Boolean 其他类型转化为布尔型代表空值，否定的值会被转换为false。
如:0 NaN Null nudefind,其余的值都会转化为true。11
```
## 运算符
```html
(1)算数运算符:+ - * / %
(2)前置自增自减运算符:++num --num (前置先加1后返回值)
(3)后置自增自减运算符num++ num-- (后置返回原值后加1)
(4)比较运算符:< > >= <= = != === !==
(5)逻辑运算符:&&与 ||或 !非
重点:= 赋值,把右边的值给左边
    == 比较,段段两边的指示不相等
    ===全等,判断两边的值和数据类型是否完全相等
```
## 流程控制-if语句
```html
(1)if语句 语法:if(条件表达式){执行语句}
(2)if else语句 语法:if else(条件表达式){条件执行成立的代码}else{条件不成立时执行的代码}
(3)if else if语句 语法:if(){}else if(){}else if(){}else{}
```
## 三元表达式
```html
语法:条件表达式?表达式1:表达式2
例:num>5?"大于":"不大于";
执行思路:如果条件表达式为真，则返回表达式1的值，如果条件表达式的结果为假，则返回表达式2的值。
```
## 流程控制-switch语句
```html
语法:switch(表达式value值){case value值:
                         执行语句1;
                         break;
                         default:执行最后的语句}
执行思路:利用表达式的值和case后面的选项值相匹配，如果匹配上就执行该case里面的语句，如果都没有匹配上，那么执行default里面的语句。
switch注意事项:
1.在开发时表达是我们经常写成变量
2.num的值和case里面的值相匹配的时候是全等，必须是和值的数据类型一致
3.break如果当前case里面没有break不会退出switch,是继续执行下一个case
```
## switch和if else if语句区别
```html
1.一般情况下，他们两个语句可以相互替换
2.switch...case语句通常处理case为比较确定值的情况,而if...else语句更加灵活,常用于范围判断(大于等于某个范围)
3.switch语句进行条件判断后直接执行程序的条件语句效率更高。而if...else语句有几种条件就得判断多少次。
4.当分支比较少时,if...else语句执行效率比switch语句高。
5.当分支比较多时,switch语句的执行效率比较高，而且结构更清晰。
```
## 循环-for循环
```html
在程序中，一组被重复执行的语句被称为循环体，能否继续重复执行取决于循环的终止条件。由循环体及循环的终止条件组成的语句称之为循环语句。
语法结构:for(初始化变量;条件表达式;操作表达式){循环体}
1.初始化变量就是用var声明的一个普通变量，常用于作为计数器使用。
2.条件表达式就是用来决定每一次循环是否继续执行就是终止的条件。
3.操作表达式是每次循环最后执行的代码，通常我们用于计数器变量进行更新。
```
## 循环-while循环
```html
语法结构:while(条件表达式){循环体}
```
## continue关键字
```html
continue关键字用于立即跳出本次循环，继续下一次循环(本次循环中continue之后的代码就会少执行一次)
```
## break关键字
```html
break关键字用于即跳出整个循环(循环结束)
```
## 数组
```html
创建数组（1):var 数组名=new Array（）利用new创建数组
创建数组(2):var 数组名=[] 利用字面量创建数组
```
## 数据的索引
```html
用来访问数组元素的序号(数组下标从0开始)
```
## 获取数组元素
```html
数组名[索引号]
```
## 新增数组元素
```html
修改数组的长度:数组名.length=要修改的数量
追加数组的元素:数组名[索引号]=[数组元素]
```
## 函数的概念
```html
在JS里面可能会定义非常多的相同代码或者功能相似的代码，这些代码可能需要大量重复使用，虽然for循环语句也能实现一些简单的重复操作，但是比较具有局限性，此时我们可以使用JS中的函数。
函数就是封装了一段，可被重复调用执行的代码块，通过此代码块可以实现大量代码的重复使用。
```
## 声明函数
```html
语法:function 函数名(){函数体}
注意事项:
1.function声明函数的关键字全部小写。
2.函数是做某件事，函数名一般是动词。
3.函数不调用自己不执行。
```
## 调用函数
```html
语法:函数名()
```
## 函数的封装
```html
函数的封装是把一个或多个功能通过函数的方式封装起来，对外只提供一个简单的接口。
```
## 函数的参数
```html
形参 function 函数名(形参1,形参2){}形式上的参数接收实参
实参 函数名(实参1,实参2)  实际的参数
函数在声明时,可以在函数名称后面的小括号添加一些参数，这些参数被称为形参，而在调用该函数时，同样也需要传递相应的参数，这些参数被称为实参。
参数的作用:在函数内部某些值不能固定，我们可以通过参数在调用函数时传递不同的值进去
```
## 函数形参和实参个数不匹配的问题
```html
实参个数等于形参个数:输出正确结果。
实参个数多于形参个数:只取道形参的个数。
实参个数小于形参个数:多的形参定义为undefined结果为NaN。
```
## 函数的返回值return
```html
return语句:有的时候我们会希望函数将值返回给调用者，此时通过使用return语句就能实现。
语法:return 需要返回的结果(形参)
```
## return注意事项
```html
1.return语句之后的代码不会被执行(终止函数)
2.return只能返回一个值，如果用逗号隔开或者多个值,以最后一个为准。
3.函数没有return返回undefined
4.函数有return则返回undefined
```
## break continue return的区别
```html
break:结束当前的循环体(如for和while)。
continue:跳出本次循环继续执行下次循环(如for和while)。
retrun:不仅可以跳出循环，还能够返回return语句中的值，同时还可以结束当前的函数体内的代码。
```
## arguments的使用
```html
当我们不确定有多少个参数传递的时候，可以使用arguments来获取在js中Arg ments，实际上它是当前函数的一个内置对象。所有函数都内置了一个arguments对象，argument对象中储存了传递所有实参。
arguments显示是一个为数组，因此可以进行遍历为数组具有以下特点:
1.所以索引存方式储数据。
2.不具有数组push pop等方法。
3.只有函数才有argument对象。
```
## 声明函数(2)
```html
语法:var 变量名 =function(){}
```
## 创建对象的三种方式
```html
(1)利用字面量创建对象   var obj={属性1:值,属性2:值}
1.里面的属性或方法，我们采取键值对的形式,键 属性名:值 属性值
2.多个属性或方法，中间用逗号隔开
3.方法冒号后面跟的是一个匿名函数
```
## 使用对象
```html
1.调用对象的属性我们采用 对象名.属性名
例:alert(ojb.uname)
2.调用属性还有一种方法  对象名["属性名"]
例:alert(obj["age"])
3.调用对象函数的方法  对象名.函数名()
例:obj.getkey()
```
## 构造函数
```html
构造函数是一种特殊的函数，主要用来初始化对象，即为对象成员变量赋初始值，它总与new运算符一起使用。我们可以把对象中一些公共属性和方法抽取出来，然后封装到这个函数里面。
语法格式:
function 构造函数名(){
         this.属性=值
         this.方法=function(){}
}
使用构造函数:new 构造函数名()
注意事项:构造函数名首字母要大写,构造函数不需要return,调用构造函数必须使用new属性和方法，必须添加this。
代码验证:
function Star(uname,agr,sex){
this.name=uname
this.age=age
this.sex=sex
}
var ldh=new Star("刘德华","18","男")
```
## new关键字执行过程
```html
1.new构造函数可以在内存中创建一个空的对象
2.this就会指向刚才创建的空对象
3.执行构造函数里面的代码给这个空对象添加属性和方法
4.返回这个对象(所以构造函数里面不需要return)
```
## 遍历对象
```html
for...in语句用于数组或者对象的属性进行循环操作。
语法:for(变量 in 对象){console.log([变量])}
使用for in里面的变量命名一般为key或者key(不强制命名)
```
## 内置对象
```html
内置对象就是指js语言自带的一些对象，这些对象供开发者使用，并提供了一些常用的或是最基本的必要的功能(属性和方法)
javaScript供了多个内置对象:Math Date Array String
```
## 查文档
```html
MDN官方网址:https://developer.mozilla.org/zh-CN
```
## Math取随机整数方法(公式)
```html
function getRandom(min,max){
return Math.floor(Math.random()*(max-min+1))+min
}
```
## Date日期对象
```html
1.Date()日期对象是一个构造函数必须使用new来调用来创建日期对象。
2.参数常用写法数字型2021，5，29或是字符串型“2021－5－29 8:8:8”。
3.Date实例用来处理日期和时间，获取当前时间必须实例化
var now =new Date()
```
## 日期格式化
```html
var date=new Date() 声明日期对象函数
get FullYear()  获取当年
get Month()     获取当月(0-11)
get Date()      获取当天日期
get Day()       获取星期几(0－6)
get Hours()     获取当前小时
get Minutes()   获取当前分钟
get Seconds()   获取当前秒钟
```
## 四种获得总的毫秒数
```html
valueOf（）      get Time()
+new Date()     Date.now()
例:console.log(date.getFullYear())
   console.log(date.valueOf)
```
## 总毫秒数转换为天、时、分秒公式
```html
d=parseInt(总秒数/60/60/24) 计算天数
h=parseInt(总秒数/60/60%24) 计算小时
m=parseInt(总秒数/60%60)    计算分钟
s=parseInt(总秒数%60)       计算当前秒数
```
## 检测是否为数组
```html
1.instance of 运算符  语法:数组名.instance of Array
2.Array.isArray()    语法:Array.is Array(数组名)
提示:第二种是H5新增的 IE9以上才可以用
```
## 添加数组元素
```html
1.push() 在数组中的尾末添加一个或多个数组元素
(1)push是可以给数组追加新的元素
(2)push()参数直接写数组元素
(3)push完毕之后返回的结果写新的长度
(4)原数组也会发生变化
2.unshift()在数组开头添加一个或多个数组元素
例:数组名.push(5,"1")
```
## 删除数组元素
```html
1.pop()删除数组最后一个元素
(1)pop()是可以删除数组的最后一个元素，一次只能删除一个元素
(2)pop()没有参数
(3)pop()完毕后返回的结果是删除的那个元素
(4)原数组也会发生变化
2.shift()删除数组第一个元素
例:数组名.pop()
```
## 数组排序
```html
1.reverse() 翻转数组   语法:数组名.reverse()
2.sort() 冒泡排序      语法:数组名.sort()
```
## sort解决方案
```html
var arr1=[13,4,76,1,2]
arr1.sort(function(a,b){
return a-b  
})
a-b升序的顺序排序       b-a降序的顺序排序
```
## 数组索引方法
```html
indexOf() 作用就是返回该数组元素的索引号(从前面开始查找)
(1)他只满足第一个满足条件的索引号
(2)他如果在该数组里面找不到元素，则返回-1
2.lastIndexOf()作用就是返回该数组元素的索引号（从后往前）
```
## 数组转换为字符串
```html
1.tostring()   语法:数组名.tostring()
2.join()       语法:数组名.join("-")
```
## 字符串操作方法
```html
1.concat() 用于连接两个或多个字符串，拼接字符串等。
2.substr(start,length)从start位置开始(索引号)，length取的个数。
例:var start1="你好，世界"
alert(start1.substr(3,2))
```
## 获取元素的方式
```html
1.根据ID获取元素               2.根据标签名获取
3.通过HTML5新增的方法获取       4.特殊元素获取
console.dir 打印返回元素对象更好的查看里面的属性和方法
获取元素ID：document.getElementById()
获取标签名:document.getElementsByTagName()
获取元素class:document.getElementsByClassName()
获取选择器:document.querySelector()
获取所有选择器:document.querySelectorAll()
获取body元素:document.body
获取html元素:document.doucumentElement
```
## 事件三要素
```html
(1)事件源,事件被触发的对象,谁,按钮。
(2)事件类型 如何触发 什么事件 比如鼠标点击(onclick)。
(3)事件处理程序,通过一个函数赋值的方式完成。
```
## 执行事件的步骤
```html
(1)获取事件
(2)注册事件
(3)添加事件处理程序(采用函数赋值方式)
```
## 常见鼠标事件
```html
onclick    鼠标点击左键触发  onmouseover 鼠标经过触发
onmouseout 鼠标离开触发     onfocus  获得鼠标焦点触发
onblur     失去焦点触发     onmousemove 鼠标移动触发
onmouseup  鼠标弹起触发     onmousedown 鼠标按下触发
```
## 操作元素
```html
JavaScript的DOM操作可以改变页面内容结构和样式，我们可以利用DOM操作元素来改变元素里的内容，属性等。
element.innerText  改变元素内容
element.innerHTML  改变元素内容
```
## 常见的元素属性操作
```html
src href id alt title 等
```
## 获取属性值
```html
element.属性  //获取内置属性值（元素本身自带的属性）
element.getAttribute("属性") //主要获取自定义的属性
```
## 设置属性值
```html
element.属性=“值” //设置内置属性值
element.setAttribute(“属性”，“值”)//设置自定义属性值
```
## 移除属性
```html
element.removeAttribute(“属性”)
自定义属性目的是为了保存并使用数据，有些数据可以保存到页面中，而不用保存到数据库中。
H5自定义属性书写规范:data-开头，做为属性名并且赋值。
例:data-index1=“1”
```
## 节点操作
```html
document.createElement(“li”) 创建元素节点
document.appendChild(child) 添加元素节点
node.inserBefore(child,指定元素) 添加元素节点到最前面
node.removeChild(child) 删除节点
例：var li=document.createElement(“li”)
   ul.appendChild(li)
   li.innerHTML=text.value
   或ul.insertBefore(li,ul.children[0])
```
## 阻止链接默认跳转
```html
JavaScript:void(0);或者javascript:;
```
## 复制节点(克隆节点)
```html
node.cloneNode() 方法返回调用该方法节点的副本
例:var lili=ul.children[0].cloneNode(true)
   ul.appendChild(lili)
   注意:括号为空或者false是浅拷贝，只复制标签，不复制里面的内容。
```
## 注册监听事件
```html
eventTarget.addEventListener(type,listent,[useCapture])
eventTarget.addEventListener()方法将指定的监听到eventTarget(目标对象上)该对象方法接收三个参数：
type:事件类型字符串，比如click mouseover注意这里不能带on
listener:事件处理函数事件发生时会调用该监听函数。
useCapture：可选参数是一个布尔值默认是false。
```
## 删除事件
```html
传统解除事件:eventTarget.onclick=null
监听解除事件:eventTarget.removeEventListener(type,listener[useCapture])
```
## 事件对象 event
```html
1.event就是一个事件对象写到侦听函数的小括号里当形参来看。
2.事件对象只有有了事件才会存在，它是系统给我们自动创建的，不需要我们传递参数。
3.事件对象是事件一系列相关数据的集合，跟事件相关的。
4.这个事件对象我们可以自己命名e event evt等。
官方解释:event对象代表事件的状态，比如键盘的状态，鼠标的位置，鼠标按钮的状态。
简单理解:事件发生后，跟事件相关的一系列信息数据的集合者放到这个对象里面，这个对象就是事件对象event它有很多属性和方法。
```
## this和e.target的区别
```html
this哪个元素绑定了这个事件那么就返回谁。
e.target点击了哪个元素就返回哪个元素？
```
## 事件对象的常见属性和方法
```html
e.returnValue 该属性阻止默认行为
e.preventDefault()该方法阻止默认行为(标准)
e.stopPropagation()阻止冒泡
e.canceBubble 该属性阻止冒泡
e.type 返回事件的类型 比如:click mouseover
e.srcElement 返回触发事件对象
e.target 返回触发事件的对象(标准)
```
## 禁止选中文件和禁止右键菜单
```html
(1)contextmenu 禁止右键菜单
例:document.addEventListener("contextmenu",function(e){e.preventDefault()})
(2)selectstant 禁止选中文字
例:document.addEventListener("selectstant",function(e){e.preventDefault()})
```
## 鼠标事件对象
```html
e.clientX 返回鼠标相对于浏览器可视窗口的X坐标
e.clientY 返回鼠标相对于浏览器可视窗口的Y坐标
e.pageX 返回鼠标相对于文档页面的X坐标
e.pageY 返回鼠标相对于文档页面的Y坐标
e.screenX 返回鼠标相对于电脑屏幕的X坐标
e.screenY 返回鼠标相对于电脑屏幕的Y坐标
```
## 常用键盘事件
```html
onkeyup 某个键盘按键被松开时触发
onkeydown 某个键盘按键被按下时触发
onkeypress 某个键盘按键被按下时触发(不识别功能键，如Ctrl shift等)
三个事件的执行顺序:keydown-keypress-keyup
```
## 键盘事件对象
```html
keyCode  返回该键的ASCLL值
```
## BOM
```html
window.onload 是窗口加载事件，当文档内容完全加载完成会触发该事件，就会调用处理。
window.onload传统注册事件方式只能写一次，如果有多个会以最后一个为准。
如果使用addEventListener则没有限制。
(1)window.addEventListener("load",function(){})
(2)document.addEventListener("DOMContentLoaded",function(){})
(3)window.onload=function(){}
1.load等页面内容全部加载完成,包含页面DOM元素图片flash css等。
2.DOMContentLoaded是DOM加载完毕，不包含图片 flash css等就可以执行。
```
## 调整窗口大小事件
```html
window.addEventListener("resize",function(){})
1.只要窗口大小发生像素变化，就会触发这个事件。
2.我们经常利用这个事件完成响应式布局window.innerWidth 当前屏幕的宽度。
```
## 定时器
```html
(1)setTimeout() 定时器
window.setTimeout(调用函数,[延迟的毫秒数])
setTimeout()方法用于设置一个定时器,该定时器到期后执行调用函数。
1.window在调用的时候可以省略。
2.这个延时事件单位是毫秒也可以省略，默认是0
3.页面中可能有很多定时器，可以给定时器声明一个变量。
(2)clearTimeout 清除定时器
window.clearTimeout(timeoutID)
(3).setInterval() 定时器
window.setInterval(回调函数,[延时的毫秒数])
(4).clearInterval 清除定时器
重点：setTimeout和setInterval区别
1.setTimeout延时事件到了,就去调用这个函数，只调用一次，就结束了这个函数。
2.setInterval每隔这个延迟时间就去调用一次回调函数，会调用很多次。
```
## location对象
```html
window对象给我们提供了location属性用于获取或设置窗口的URL，并且可以用于解析URL。因为这个属性返回的是一个对象，所以我们将这个属性称为location对象。
```
## URL
```html
protocol:通信协议常用的http，ftp，maito等
host:主机(域名)
port:端口号(可选)默认端口为80
path:路径由零个或多个“/”符合隔开的字符串，一般用来表示主机上的一个目录或文件地址。
query:参数以键值对的形式通过&符分隔开来。
fragment:片段#后面内容常见于链接锚点
```
## location对象属性
```html
locarion.href 获取或设置整个URL
location.host 返回主机(域名)
location.port 返回端口号
location.pathname 返回路径
location.search 返回参数
location.hash 返回片段#后面的内容
```
## location对象方法
```html
location.assign() 跟href一样，可以跳转页面（也称为重定向页面）
location.replace()替换当前页面，因为不记录历史，所以不能退页面
location.reload() 重新加载页面,相当于刷新按钮或这f5，为true强制刷新
```
## 中文转换为字符串
```html
var res=encodeURLComponent("张三")
```
## navigator对象
```html
navigator对象包含有关浏览器的信息，他有很多属性，我们最常用的就是userAgent该属性，可以返回由客户机发送服务器的user－agent头部的值。
下面的代码可以判断用户哪个终端打开页面就跳转到哪个：
if((navigator.userAgent.match(/(phone|pad|pod|iPhone|iPod|ios|iPad|Android|  
Mobile|BlackBerry|IEMobile|MQQBrowser|JUC|Fennec|wOSBrowser|BrowserNG|  
      WebOS|Symbian|Windows Phone)/i))) {
            window.location.href = ""; //手机端
          }  
 else{  
      window.location.href=""; //电脑端
  }
```
## history对象
```html
window对象给我们提供了一个history对象，与浏览器历史进行交互，该对象包含用户在浏览器窗口中访问过的URL。
back() 可以后退功能
forward() 忘了啥功能，自己百度
go() 也忘了
```
## 本地存储特性
```html
1.数据存储在用户浏览器中
2.设置、读取方便、甚至页面刷新不丢失数据
3.容量较大，session storage 约5M local storage约20M
4.只能存储字符串，可以将对象json.stringify()编码后存储。
(1)存储数据:sessionStorage.setItem("key",value)
(2)获取数据:sessionStorage.getItem("key")
(3)删除数据:sessionStorage.removeItem("key")
(4)删除所有数据:sessionStorage.clear("key")
———————————————————————————————————————————————
(1)存储数据:localStorage.setItem("key",value)
(2)获取数据:localStorage.getItem("key")
(3)删除数据:localStorage.removeItem("key")
(4)删除所有数据:localStorage.clear("key")
注:所有的key自定义,value是变量
```
