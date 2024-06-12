## Vue的基本使用
```html
(1)导入vue.js文件的script脚本
(2)在页面中声明一个将要被vue所控制的DOM区域
(3)创建一个vm实例对象
<body>
<div id="app">{{username}}</div>
<script>
//创建vue实例对象
const vm=new Vue({
el:“#app”,
data:{},
methods:{
函数名(){}
},
})
</script>
</body>
1:el属性是固定的写法,表示vm实例要控制页面上的哪个区域，接收的值是一个选择器。
2:data对象就是要渲染到页面上的数据。
3:methods的作用就是定义事件的处理函数。
```
## Vue调试工具以及组件库
```html
安装vue－devtools 调试工具
day.js时间库 :https://dayjs.fenxianglu.cn/category/
Element-ui :https://element.eleme.cn/#/zh-CN
vant :https://vant-contrib.gitee.io/vant/v2/
axios:https://www.axios-http.cn/docs/intro
```
## Vue指令
```html
Vue的指令按照不同的用途分为如下6大类
①内容渲染指令    ②属性绑定指令    ③事件绑定指令
④双向绑定指令    ⑤条件绑定指令    ⑥列表渲染指令
```
## Vue指令说明
```html
v-model 双向数据绑定       v-on 监听事件
v-bind 单向数据绑定        v-text 插入文本内容
v-html 插入包含HTML的内容  v-for 列表循环
v-if 条件渲染             v-show 显示隐藏
```
## 内容渲染指令
```html
内容渲染指令用来辅助开发者渲染DOM元素的文本内容。常用的内容渲染指令如:v-text  {{}}  v-html
语法:
<p v-text=""></p>
{{}}
<p v-html=""></p>
注意：
(1)v-text指令的缺点会覆盖元素内部原有的内容
(2){{}}指令是插值表达式，专门用来解决v-text会覆盖默认文本内容的问题。
(3)v-text和插值表达式只能渲染纯文本内容,如果要把包含HTML和字符串的渲染页面的HTML元素，则需要用到v-html。
```
## 属性绑定指令
```html
<input type="text” v-bind:placeholder="">
注意:
(1)如果需要为元素的属性动态绑定属性值，则需要用到v-bind属性绑定指令。
(2)也可以简写成“:”。
(3)在使用v-bind使用期间需要进行动态拼接则需要用双引号包裹单元号。
```
## 事件绑定指令
```html
<button v-on:click="事件函数名"></button>
注意:
(1)Vue提供了v-on事件绑定指令,用来DOM元素绑定事件监听。
(2)在methods方法内如果要修改data里面的数据源可以通过this修改值。
(3)在绑定事件处理函数的时候，可以使用()传递参数。
(4)v-on的简写指令为“@”。
(5)vue提供了内置的变量叫做$event，它就是原生DOM的事件对象e。
```
## 事件修饰符
```html
在事件处理函数中调用event.preventDefault()或event.stopPropagation()是非常常见的需求,因此vue提供了修饰符的概念，常用的五种修饰符如下:
.prevent 阻止默认行为(例如:阻止a链接跳转，表单的提交等)
.stop 阻止事件冒泡
.capture 以捕获模式触发当前的事件处理函数
.once 绑定的事件只触发一次
.self 只有在event.garget是当前元素自身触发事件处理函数。
注意:
.prevent和.stop.是最常用的修饰符。
```
## 按键修饰符
```html
在监听键盘事件时，我们经常需要判断详细的按键，此时可以为键盘相关的事件添加按键修饰符。
例:<input @keyup.enter="submit()">
```
## 双向数据绑定指令
```html
vue提供了v-model 双向数据绑定指令,用来辅助在不操作DOM前提下，快速获取表单的数据。
```
## v-model指令的专用修饰符
```html
.number 将用户输入的值转为数值型
.trim  自动过滤用户输入的首尾空白字符
.lazy 在“change”时而非“input”时更新
语法:<input type="text" v-model.number="">
```
## 条件渲染指令
```html
条件渲染指令用于辅助按需控制DOM的显示与隐藏分别是:v-if和v-show。
注意:
1:v-if每一次都会动态的移除元素或动态的创建元素。
2:v-show添加或移除display;none样式。
3:如果要频繁切换样式使用v-show更好。
4:如果刚进入页面的时候某些元素不需要被展示的时候，后期这个元素有可能不需要展出出来，此时用v-if的时候性能更好。
v-if 可以单独使用,或配合v-else指令一起使用。
v-else指令必须配合v-if指令一起使用，否则它将不会被识别。
v-else-if指令出现率很低一般用不到，除非判断条件很多。
```
## 列表渲染指令
```html
vue提供了v-for列表渲染指令，基于用来一个数组来循环渲染一个列表结构，v-for指令需要用item in items形式的特殊语法。
item:是待循环的数组变量名
items:是被循环的每一项
v-for指令还支持一个可选的第2个参数，当前项的索引，
语法:v-for”(item,index)in items”:key=""
官方建议:只要用到v-for指令，那么就一定要绑定一个:key 属性
而且尽量把id作为key的值。
key的注意事项：
①:key的值只能是字符串或者数字型
②:key的值必须是具有唯一性的(即:key的值不能重复)
③:建议把数据项id属性的值作为key的值(因为id属性的值具有唯一性)
④:使用index的值当做key的值没有任何意义(因为
index的值不具有唯一性)
⑤:建议使用v-for 指令时一定要指定key的值。
```
## 私有过滤器(Vue3已淘汰)
```html
过滤器应该添加在JavaScript表达式的尾部，由管道符“|”进行调用，常用于文本的格式化，可以用在插值表达式和v-bind属性绑定,过滤器函数必须定义到filters节点之下，与data平级。
语法:{{message|过滤器名(自定义)}}
    filters:{
    过滤器名(形参名){return结果}
    }
    charAt()方法，这个方法接收索引值,表示从字符串中把索引对应字符获取出来。
    toUpperCase()转换为大写
    slice()方法可以截取字符串，从指定索引往后截取。
   
```
## 全局过滤器
```html
声明全局过滤器语法:Vue.filter("全局过滤器的名字","全局过滤器的处理函数")
 注意点:
    1.要定义到filters节点下，本质是一个函数。
    2.在过滤器函数中,一定要有return值。
    3.在过滤器的形参中,就可以获取到管道符前面的待处理的值。
    4.如果全局过滤器和私有过滤器名字一致，此时就按“就近原则”，调用的是私有过滤器。
```
## watch 侦听器
```javascript
语法:watch:{
  uservalue(oldval,newval)
}
注意:
1.侦听器本质上是一个函数,要监视哪个数据的变化，就把数据名作为方法即可。
2.新值在前，旧值在后。
3.应用场景用于用户名是否被占用
4:immediate选项的默认值是false
5.immediate的作用是控制侦听器是否自动触发一次。
6.可以通过deep选项让助听器深度侦听对象中每个属性的变化。
```
## computed 计算属性
```html
1.所有的计算属性,都要定义到computed节点之下。
2.计算属性在定义的时候,要定义成方法格式。
```
## axios
```javascript
axios中文官网:http://www.axios-js.com
axios的基本语法:
document.querySelector("#id名").addEventListener("click",async function(){
const {data:res}=await axios({
method:"请求的类型",
url:"请求的URL地址",
params:{}
data:{}
})
con
})
注意:
1.发起GET请求用params:{}
2.发起POST请求用data:{}
3.await只能用在被async修饰的方法中
4.把解构出来的data属性使用冒号进行重新命名,一般都重命名为:data:res。
```
### axios.get和axios.post
```javascript
axios.get语法:
const{data:res}=await axios.get("url"{params:{}})
axios.post语法:
const{data:res}=await axios.post("url",{}
```
### axios挂载到vue原型上并配置请求根路径
```javascript
在main.js文件中导入
import axios from ‘axios’
//全局配置axios的请求根路径
axios.defaults.baseURL='请求根路径'
//把axios挂载到Vue.prototype上，每个.vue组件的实例直接使用。
Vue.prototype.axios=axios
今后在每个vue组件中要发起请求，直接调用this.axios.xxx
例:const {data:res} =await this.axios.get('')
```
## 单页面应用程序
```html
单页面应用程序(英文名: Single Page Application)简称SPA，顾名思义，指的是一个Web网站中只有唯一一个HTML页面，所有的功能与交互都在唯一一个页面内完成。
```
## Vue项目构成
```html
assets文件夹:存放项目中用到的静态资源文件,例:css样式表、图片资源。
components文件夹:封装的可复用的组件都要放到components目录下。
main.js:是项目的入口文件，整个项目的执行要先执行main.js。
app.vue:项目的根组件
```
### Vue项目的运行流程
```html
在工程化的项目中,vue要做的事很单纯,通过main.js把App.vue渲染到index.HTML的指定区域中。

import Vue from "vue" //导入vue这个包,得到Vue构造函数。
import App from "./App.vue"//导入App.vue根组件，将要把App.vue中的模板结构渲染到HTML页面中。
$mount(“#app”)作用跟el:"#app"没啥区别。
render:h=>(App) //把render函数指定的组件渲染到HTML页面中。
其中:
①:App.vue用来编写待渲染的模板结构。
②:index.html中需要预留一个el区域。
③:main.js把App渲染到了index.html所预留的区域中。
```
### #vue组件的三个组成部分
```html
每个.vue组件都由3部分构成,分别是:
template->组件的模板结构
script->组件的JavaScript行为
style->组件的样式
export default{}默认导出script的固定写法
<script>
export default{
data(){
return{}
}
}
</script>
注意:
①vue组件中的data必须是一个函数。
②这个return出去的{}中，可以定义数据。
```
### 使用组件的三个步骤
```html
 1.使用import语法导入需要的组件
 import Left from "@/components/Life.vue"
 2.使用components节点注册组件
 export default{
       components:{Left}}
 3.以标签形式使用刚才注册的组件
 <div class="box">
 <Left></Left>
 </div>
```
### 注册全局组件
```javascript
在Vue项目的main.js入口文件中，通过Vue.component()方法可以注册全局组件。
语法:
//导入需要全局注册的组件
import Count from "@/components/Count.vue"
Vue.component("MyCount",Count)
参数1:字符串格式，表示组件的“注册名称”
参数2:需要被全局注册的那个组件
```
### 组件样式冲突的问题
```html
默认情况下，写在.vue组件中的样式会全局生效,因此很容易造成多个组件之间的样式冲突。
导致组件之间样式冲突的根本原因是:
①单页面应用程序中,所有组件的DOM结构都是基于唯一的index
.html页面进行呈现的。
②每个组件中的样式都会影响整个index.html页面中的DOM。
写法:<style lang="less" scoped>/deep/ 类名{}</style>
socped属性:自动为每一个标签生成date-v-数字。
在父组件中直接修改子组件的样式时需要用到/deep/，当使用第三方组件库的时候，如果有修改第三方组件库默认样式的需求，需要用到/deep/。
```
## 组件的props
```html
props是组件的自定义属性,在封装通用组件的时候合理地使用props可以极大的提高组件的复用性。
语法:props:[“自定义属性名A”,"自定义属性名B"]
<自定义标签 自定义属性名=“”></自定义标签>
{{自定义属性名}}
注意点:
①自定义属性名的值如果是数字那么要在自定义属性名前面加上“:”，否则为字符串。“:”的意思就是v-bind。
②封装的自定义属性是只读的，不能直接修改props值，否则会报错，要修改props值可以把props的值转存到data中，因为data中的数据是可读可写的。
```
### props的default默认值
```html
语法:props:｛自定义属性:{default:0}｝
注:如果外界使用自定义组件的时候没有传递值则默认值生效，如果传了值则覆盖默认值。
```
### props的type值属性
```html
在声明自定义属性时，可以通过type来定义属性值的类型。
type:Number并在自定义属性名前面加上“:"
```
### props的required必填项
```javascript
语法:props:{自定义属性:{required:true}}
```
## 生命周期
```html
生命周期(life cycle)是指一个组件从创建->运行->销毁的整个阶段，强调的是一个时间段。
生命周期函数:是由vue框架提供的内置函数，会伴随着组件的生命周期，自动按次序执行。
```
### 组件生命周期函数分类
```html
       组件创建阶段
beforeCreate 创建实例对象之前执行
created 创建实例对象之后执行
beforeMount 页面挂载成功之前执行
mounted 页面挂载成功之后执行

       组件运行阶段
beforeUpdate 组件更新之前执行
updated 组件更新之后执行

       组件销毁阶段
beforeDestory 实例销毁之前执行
destroyed 实例销毁之后执行

①beforeCreate:组件的props、data、methods 尚未被创建，都处于不可用状态。－初始化事件和生命周期函数

②created:组件的props、data、methods①创建好,都处于可用状态。但是组件的模板结构尚未生成。－初始化props、data、methods，非常常用，一般用于发送ajax，数据转存到data中。

③beforeMount:将要把内存中编译好的HTML结构渲染到浏览器中,此时浏览器中还没有当前组件的DOM结构。

④mounted:已经把内存中的HTML结构,成功渲染到当前浏览器中，此时浏览器中已经包含了当前组件的DOM结构。

⑤beforeUpdate:将要根据变化过后，最新的数据，重新渲染组件的模板结构。

⑥updated:已经根据最数据，完成了组件DOM结构的重新渲染。

⑦beforeDestroy:将要销毁此组件,此时尚未销毁,组件还处于正常工作状态。－执行后销毁当前组件，数据侦听器、子组件、事件监听。

⑧destroyed:组件已经被销毁，此组件在浏览器中对应的DOM结构已经完全被移除。
```
##  自定义事件—子向父传值
```html
  $emit(“自定义事件名称”,传给父组件的新值)		
  子组件:this.$emit('numchange',this.count)
父组件:<Son @numchange="getNewCount"></SonSon>
      data(){
         retrun{
              countFromSon:0
}
}
      getNewCount(val){
         this.countFromSon=val
}
```
##  父向子传值

```html
例：
父组件：<son :msg="message" :user="userinfo"><son/>
data(){
    return{message:"数据1",userinfo:"数据2"}
    }
    子组件:<p>父组件传过来的值是{{msg}}</p>
          <p>父组件传过来的值是{{user}}</p>
    props:["msg","user"]
```



## EventBus数据共享

```javascript
①创建eventBus.js模块,并向外共享一个Vue的实例对象
②在数据发送方，调用bus.$emit(“事件名称”，要发送的数据)方法触发自定义事件
③在数据接收方，调用bus.$on(“事件名称”，事件处理函数) 方法注册一个自定义事件
eventBus文件内容:
import Vue from "vue"
export default new Vue() //向外共享vue的实例对象
例：
兄弟组件A(数据发送方)                               兄弟组件B(数据接收方)
import bus from './eventBus.js'                import bus from './eventBus.js’
export default {                                export default{
    data(){                                     data(){
        ruturn{                                 return{
            msg:'值'                            msgFromLeft:''
        }，                                                   }
        methods:{                                              },
            sendMsg(){                                        created(){
                bus.$emit('share',this.msg)                   bus.$on('share',val=>{
            }                                                 this.msgFromLeft=val
        }                                                     })
    }                                                              }
}                                                                       }
```
## ref引用
```javascript
ref可以在不依赖于jQuery的情况下,获取DOM元素或组件的引用。
每个vue的组件实例上,都包含了一个$refs对象,里面存储着对应的DOM元素或组件的引用,默认情况下组件的$refs指向一个空对象。
语法:
            加给标签 
<h1 ref="myh1">APP</h1>
this.$refs.myh1.style.color="red" 
            加给组件
<Left ref='myLeft'> </Left>
this.$refs.myLeft.count=0
```
##   this.$nextTick(cb)方法
```javascript
组件的$nextTick(cb)方法,会把cb回调推迟下一个DOM更新周期之后执行，通俗理解是:等组件的DOM更新完成之后，在执行cb回调函数。从而能保证cb回调函数可以操作最新的DOM
```
## 数组中的some循环方法
```html
some循环在找到对应的项之后可以通过return:true固定语法可以终止some循环。
语法：
const arr=['小孩','大人','男人']
arr.some((item,index)=>{
if(item==='小孩'){
return true
}
})
```
## 数组中的every 循环方法
```html
every循环只要有任何一项不满足条件就返回false，满足则返回true。
语法：
const arr=[
{id:1,name='西瓜',state:true}
{id:2,name='苹果',state:true}
{id:3,name='梨子',state:true}
]
const result= arr.every(item=>item.state)
```
## 数组中的reduce方法
```javascript
const arr=[
{id:1,name='西瓜',state:true,price:10,count:1}
{id:2,name='苹果',state:true,price:20,count:2}
{id:3,name='梨子',state:true,price:30,count:3}
]
arr.filter(item=>item.state).reduce((amt,item)=>{
    return amt+=item.price*item.count
},0)

reduce((累加的结果，当前的循环项)=>{
return 算法
},初始值)
```
## 动态组件component标签
```html
语法:<component :is=''></component>
is:指定哪个组件就渲染哪个组件
```
## keep-alive保持状态 
```html
用法:
<keep-alive>
<component :is='' include=‘’></component>
</keep-alive>
```
### keep-alive的include属性 
```html
include属性用来指定:只有名称匹配的组件会被缓存，多个组件用逗号隔开。
```
###  keep-alive的exclude属性
```html
exclude属性指定哪些组件不需要被缓存，但是不能同时使用exclude和include属性。
```
## v-slot指令
```html
①vue官方规定每一个slot标签都要有一个name属性。
②如果省略了name属性则有一个默认名称叫default。
③v－slot后面要跟上插槽的名字
④v－slot指令不能直接用在元素身上，必须用在template标签上
⑤v－slot指令的简写形式是 #
写法:
父组件<template v-slot:插槽的name></template>
子组件<slot name='插槽名称'></slot>
```
## 私有自定义指令
```javascript
可以在directives节点下声明私有自定义组件
写法:
directives:{
          color:{
         bind(el，binding){
      el.style.color=binding.value
                }
}
①定义为color的指令，指向一个配置对象。
②当指令第一次被绑定到元素上的时候，会立即触发bind函数。
③形参中的el表示当前指令绑定到的那个DOM对象。
④binding.value是固定写法
```
## update函数
```javascript
bind函数只调用一次:当指令第一次绑定到元素时调用，当DOM更新时bind函数不会被触发。update函数会在每次DOM更新时被调用。
updata函数在directives节点内。不是钩子函数不与data平级。
写法:
update(el,binding){
el.style.color=binding.value
｝
```
## 全局自定义指令
```javascript
写法:
Vue.directive('color',function(el,binding){
el.style.color=binding.value
})
参数1:字符串，表示全局自定义指令的名字
参数2:对象，用来接收指令的参数值
```
## 路由
### 路由的工作方式
```html
①用户点击了页面上的路由链接。
②导致URL地址栏中的Hash值变化。
③前端路由监听了Hash地址的变化。
④前端路由把当前的Hash地址对应的组件渲染在浏览器中。
```
### vue-router安装和配置路由
```javascript
①安装vue-router包
npm i vue-router@3.5.2 -S
②创建路由模块
在src源代码目录下，新建router/index.js路由模块，并初始化代码：
import Vue from 'vue'
import VueRouter from 'vue-router'
Vue.use(VueRouter)
const router=new VueRouter({routes:[
{path:'/home',component:Home}
]})
export default router
③在main.js文件导入并挂载路由模块
import router from '@/router/index.js'
并在new Vue({})里输入router
④声明路由链接和占位符
只要在项目中安装了vue-router就可以使用
<router-view></router-view>这个标签。
1.routes:是一个数组，作用定义hash地址与组件之间的对应关系。
2.Vue.use()函数的作用就是来安装插件。
3.VueRouter安装为Vue项目的插件。
```
### router-link
```html
写法:
<router-link to=''></router-link>
1.当安装和配置了vue-router后就可以使用router-link来代替普通的a标签了。
2.to就代替了href属性，并在to里面可以不用写#
```
### redirect重定向 
```javascript
路由重定向指的是用户在访问地址A的时候，强制用户跳转到地址C，从而展示特定的组件页面，通过路由规则的redirect属性，指定鱼缸新的路由地址，可以很方便地设置路由的重定向。
例:{path:'/',redirect:'Home'}
当用户访问/的时候，跳转到/home对应的路由规则。
```
### children属性声明子路由和默认子路由规则
```javascript
在src/router/index.js路由模块中，导入需要的组件，并使用children属性声明子路由规则:
写法:
routers:[{
path:'/father',component:Father,
           //默认子路由
redirect:'./father/tab1',
,children:[{
path:'tab1',component:Tab1
}]
}]
```
### 默认子路由(拓展)
```javascript
默认子路由如果children数组中，某个路由规则的path值为空字符串，则这条子路由规则叫做默认子路由。
写法:{path:'',component:Tab1}
```
### 动态路由匹配
```html
动态路由指的是:把Hash地址中可变的部分定义为参数项,从而提高路由规则的复用性。
在vue-router中使用英文的冒号(:)来定义路由的参数项。
例:{path:'./movie/:id',component:Movie}
this.$route是路由的参数对象
this.$touter是路由的导航对象
```
### 路由props传参
```html
写法:{path:'/movie/id',component:Movie,props:true}
可以为路由规则开启props
```
### 拓展query和fullPath
```html
①在hash地址中/后面的参数项，叫做‘路径参数’。
②在路由参数对象中需要使用this.$route.params来访问路径参数。
③在hash地址中,?后面的参数项，叫做‘查询参数’。
④在路由参数对象中需要使用this.$route.query来访问查询参数。
⑤在this.route中path只是只是路径部分,fullPath是完整地址
```
### vue-router 中的编程式导航API
```javascript
①this.$router.push('hash地址') 
跳转到指定的hash地址，并增加一条历史记录
②this.$router.replace('hash地址')
跳转到指定的hash地址,并替换掉当前的历史记录
③this.$router.go(数值 n)
调用this.$router.go()方法,可以在浏览历史中前进和后退
$router.go的简化用法
$router.back() 在历史记录中，后退到上一个页面
$router.forward() 在历史记录中,前进到下一个页面
```
## 导航守卫 
### 全局前置导航
```javascript
1.创建路由实例对象
const router =new VueRouter({})
router.beforeEach((to,from,next)=>{})
①调用路由实例对象的beforeEach方法，即可声明‘全局前置守卫’
②每次发生路由导航跳转到时候,都会自动触发fn这个回调函数
```
### 守卫方法3个形参
```html
to:是将要访问的路由的信息对象
from:是将要离开的路由的信息对象
next:是一个函数,调用next()表示放行,允许这次路由导航
```
### next函数的3中调用方式
```html
①当前用户拥有后台主页的访问权限，直接放行：next()
②当前用户满意后台主页的访问权限,强制其跳转到登录页面:next('/login')
③当前用户没有后台主页访问权限,不允许跳转到后台主页:next(flase)
```

