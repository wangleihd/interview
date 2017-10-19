# 目录

* [HTML-5](#HTML5)
* [CSS-3](#CSS3)
* [JavaScript](#JavaScript)
* [React](#React)
* [React Native](#ReactNative)




# 1. HTML5


## HTML全局属性有哪些
1. class: 为元素设置类标识，多个类名用空格分开
1. contenteditable: 指定元素内容是否可编辑
1. contextmenu: 自定义鼠标右键弹出内容
1. data-* : 为元素增加自定义属性
1. dir: 设定元素文本方向
1. draggable: 设定元素是否可拖拽
1. id: 元素文档内唯一
1. spellcheck: 是否启动拼写检查
1. style: 行内CSS样式
1. tabindex: 设置元素可以获得焦点, 可通过tab导航


## HTML5优缺点
优:  - W3C推荐, 网络标准统一
        - 多设备,跨平台, 改进用户体验
        - 增加新标签, 有助于开发人员定义重要内容
        - 带来更多的多媒体元素,音频视频, 替代flash
        - 对搜索引擎友好, 可用于移动应用和游戏
缺: - 浏览器支持情况不一, 兼容性不好


## 行内元素和块级元素有哪些?

1. 行内元素：span a img input i u b strong del ins
1. 块级元素: div p h1-h6 ul li ol

## 标签选择器 类选择器 id选择器 通配选择器
优先级：!important > style(行内样式) > id > class > 标签　> 继承 > 浏览器默认


## IE8以下的盒子模型元素宽高包括padding和border.

## display:none 和visibility:hidden区别

后者占位前者不占


## 用过哪些浏览器,内核分别是什么
1. IE:  trident内核
1. chrome,Opera:  Blink(基于webit, 共同开发)
1. Firefox: gecko内核
1. Safari: webkit内核
引擎主要分为渲染引擎(静态), js引擎(动态)

## doctype中HTML和XHTML的区别：
XHTML严格规范标签大小写，属性值加引号等等，用来规范语法HTML是一种基本的WEB网页设计语言，XHTML是一个基于XML的置标语言.

* 最主要的不同：

1. XHTML 元素必须被正确地嵌套。
1. XHTML 元素必须被关闭。
1. 标签名必须用小写字母。
1. XHTML 文档必须拥有根元素。



## HTML与XHTML的区别:XHTML必须正确嵌套,必须闭合,标签名小写,必须有跟元素?


## 事件委托,举例说明事件委托

使用事件委托技术能让你避免对特定的每个节点添加事件监听器；相反，事件监听器是被添加到它们的父元素上。事件监听器会分析从子元素冒泡上来的事件，找到是哪个子元素的事件。父元素上注册事件的回调函数的形参event.target就可以找到真正触发事件的子元素


## http的状态码.
```js
  1xx:  Informational(信息状态码)　　   接受的请求正在处理
  2xx:  Success(成功状态码)　　　　　    请求正常处理完
  3xx:  Redirection(重定向状态码)       需要进行附加操作以完成请求
  4xx:  Client Error(客户端错误状态码)   服务器无法处理请求
  5xx:  Server Error(服务器错误状态码)　　服务器处理请求出错
```



## get和post的区别?

## HTML5中的存储方式?

```
  cookies
  localStorage
  sessionStorage
```


## 简单说一下浏览器的本地存储
Web Storage包括sessionStorage和localStorage,具有相同的方法,如:setltem, getltem, removeltem.

在较高的浏览器版本中,js提供了sessionStorage和globalStorage.  在HTML5中提供了localStorage来取代globalStorage.


sessionStorage用于本地存储一个会话中的数据, 这些数据只有在同一个会话中的页面才能访问, 会话结束后会销毁,不是持久化的本地存储.


localStorage用于持久化的本地存储, 除非主动删除, 否则永远不会过期.



# 2. CSS3

## 浮动和它的工作原理, 如何清楚浮动
脱离文档流, 不占据空间 碰到包含的边框或浮动元素的边框停留
1. 空标签. 浮动标签后面添加空标签, 设CSS clear: both
1. 使用overflow. 给包含浮动元素的父标签添加CSS overflow:auto; zoom:1; zoom:1用于兼容IE6
1. 使用after伪对象清除
1. 设置overflow为hidden或auto

## css中link和@import区别:
link是HTML标签,@import是CSS提供的页面加载时, link会同时加载, 而@import引用的会在页面加载完后再加载link无兼容问题, 而@import只有IE5以上识别.


## CSS3新特性
```
圆角(border-radius),
阴影(box-shadow),
文字特效(text-shadow),
渐变(gradient),
旋转(rotate),
缩放(scale),
定位(translate),
倾斜(skew),
选择器,
多背景rgba,
伪类(::selection),
媒体查询.
```



## doctype的作用(多少种类型), 严格模式和混杂模式的区分,有何意义?
1. 声明用于文档最前面, 告知浏览器以何种模式来渲染文档
1. 严格模式的排版和js运作模式是以浏览器最高标准来运行的
1. 在混杂模式中, 页面以宽松的向后兼容的方式显示, 模拟老浏览器防止站点无法工作
1. 没有声明会导致文档以混杂模式呈现.








## 为什么要初始化CSS样式

浏览器兼容问题, 不同的浏览器对有些标签的默认值是不同的, 不初始化会出现差异 {padding: 0; margin:0}



## 说说对语义化的理解
1. 没有样式时候仍然能够让页面有清晰的结构
1. 有利于SEO:和搜索引擎建立良好的沟通,利于爬虫抓取更多有利信息
1. 方便其他设备解析(屏幕阅读器, 盲人阅读器)
1. 便于团队开发维护



## base64

## utf-8和unicode的区别


## 什么是响应式布局? 有那些常用的框架?

## div垂直居中的方法

1. 一个父div设置相对定位 relative，
1. 一个子div设置绝对定位 absolute，left,top都为50%,不知道自身宽高时可以用
1. transform:translate(-50%,50%);
1. 知道宽高时可以用margin-left:-selfwidth*50%;margin-top:-selfheight*50%;

## HTML常见的兼容性问题
针对ie浏览器设置的,html5shiv, respond 用于让第版本的ie浏览器支持html5的新元素和媒体查询.

```html
<!--[if lt IE 9] -->
<script src="./js/html5shiv.min.js"></script>
<script src="./js/1.4.2/respond.min.js"></script>
<!--[endif]-->
```









# 3. JavaScript

## JS基本语法知识
1. js的数据类型，存储方式(栈，堆)
2. js内置对象
3. js基本代码规范
4. call和apply作用，区别
5. push pop shift unshift
6. 媒体查询
7. this
8. js原型，原型链
9. 如何实现继承
10. 创建对象的方式
11. null \ undefined
12. ['1','2','3'].map(parseInt)
13. 事件是什么，冒泡捕获，如何阻止
14. 闭包，好处
15. 'use strict',
16. new操作符具体干了些什么
17. object.hasOwnProperty 查找对象是否有该属性名，返回布尔值，且不找原型
18. json
19. ajax
20. 同步异步，异步加载js
21. 跨域
22. es6 class
23. document.write \ innerHTML
24. DOM操作
25. 内存泄露
26. 判断当前脚本运行环境
27. 检测浏览器版本
28. canvas svg
29. 模块化规范，CommonJS, AMD, CMD
30. MVC, MVVM




## js怎么写枚举？
```js
var WeekDay = {};
WeekDay.Sunday = 0;
WeekDay.Monday = 1;
WeekDay.Tuesday = 2;
WeekDay.Wedesay = 3;
WeekDay.Thursday = 4;
WeekDay.Friday = 5;
WeekDay.Saturday = 6;
```


## 写一个js数组去重方法.
```js

```

## es5模拟生成一个类 Person,有两个属性v1,v2,两个方法f1,f2;
**ES5**
```js
    function Person(){
      this.v1 = "v1";
      this.v2 = "v2";
      this.f1 = function(){}
      this.f2 = function(){}
    }
```
**ES6生成一个类 Person,有两个属性v1,v2,两个方法f1,f2;**

```js
  class Person(){
    construct(v1,v2){
      this.v1 = v1
      this.v2 = v2
    }
    f1(){}
    f2(){}
  }
```


## 用ajax发送请求数据 {name:"lisi"},成功打印name的值,失败打印请求失败
```js
    $.ajax({
        url:"localhost",
        method:"get",
        data:{
          name:"lisi"
        }
      }).done(function(data,textstatus,as){
          console.log("name : " + data.name)
      }).fail(function(a,b,c){
          alert("请求失败")
      })
```

## ajax跨域的解决方案有哪几种？
jsonp  cors  websocket

## 什么是闭包, 闭包的优点, 闭包跟匿名函数的区别, 作用链-原型链 (现实原理)
```js

```

## fetch()方法干什么用的，是否对该方法进行了封装？发生错误是怎么处理的？



## js的数据类型有哪些？哪些是原生数据类型？哪些是引用数据类型？


## 什么是作用域链？什么是原型链？什么是闭包？


## ES6的新特性有哪些？

## ES6中常用的数据结构，特意说了map，还问了数组去重(set方法)。


## 动手实现Array.prptotype.sort()方法，即数组排序？


## es6 实现链表数据结构，具有append(),insert(),remove()方法.


## 写一个简单的闭包，说说对闭包的理解

闭包就是有权访问另一个函数作用域中的私有变量的函数


```js
function closure(){
    var a = 10;
    return function(){
      console.log(a)
    }
  }
  var win = closure();
  win();
```


## 下面的代码会输出什么?
```js
function test(a, b){
  console.log(b);
  return {
    test:function(x){
      return test(x, a);
    }
  };
}
```

**写出如下代码运行结果:**
```js
 var a = test(0); a.test(1); a.test(2); a.test(3);
 var b = test(3).test(2).test(1).test(0);
 var c = test(2).test(3); c.test(1); c.test(0);
```

答:这是一个闭包经典问题，直接调用test()函数那么只执行到console.log(b)，若a.test(n)那么则会运行return内的函数.


## 参考如下代码，写出最后运行结果。
```js
function Yjhl(){
  getNumber = function(){
  console.log(1);
  return this;
  }
}
Yjhl.getNumber = function(){
  console.log(2);
}
Yjhl.prototype.getNumber = function(){
  console.log(3);
}
var getNumber = function(){
  console.log(4);
}
function getNumber(){
  console.log(5);
}
```

**请写出以下输出结果:**

```js
Yjhl.getNumber();
getNumber();
Yjhl().getNumber();
getNumber();
new Yjhl.getNumber();
new Yjhl().getNumber();
new new Yjhl().getNumber();
```

答:该题首先定义了一个Yjhl函数，之后为Yjhl创建了一个叫getName的静态属性存储了一个匿名函数，之后为Yjhl的原型对象创建了一个叫getName的匿名函数。
之后又通过函数变量表达式创建了一个getName函数，最后再声明一个叫getName函数。


第一个问题 Yjhl.getNumber() 是直接访问Yjhl函数上的存储的静态属性，所以是2。


第二个问题 getNumber(),也就是直接调用getNumber函数，var getNumber 与 function getNumber() 都会发生声明提升，所以最后未提升的是变量的值，
也就是 function(){ console.log(4)},所以输出getNumber()的值为 4。


第三个问题 Yjhl().getNumber();先执行Yjhl函数，然后调用Yjhl函数返回值对象的getNumber属性函数。因为Yjhl()函数中getNumber没有var声明，所以会像作用域内
寻找getNumber变量，没有找到，再像当前作用域上层寻找，这里找到的就是console.log(4);并且重新赋值为 console.log(1)
,而Yjhl返回值是this，此时this就是window
所以window上调用getNumber()则会打印console.log(1);


第四个问题 getNumber()是直接调用window.getNumber(),而此时的var getNumber()的值已经被修改了，所以打印结果也是 console.log(1)


第五个问题 new Yjhl.getNumber();此处考察的是js的运算符优先级问题。因为 . 的优先级高于new,所以想当是 new (Yjhl.getNumber)();相当于作为构造函数来执行
所以打印 console.log(2)。


第六个问题 new Yjhl().getNumber();因为()括号的优先级高于new，所以相当于(new Yjhl()).getNumber(),此时就会先调用Yjhl()，但此时的构造函数有返回值，这时要看返回值的数据类型是否为引用类型。
this在构造函数中本身就代表实例化对象，所以直接返回实例化对象，但是该构造函数没有定义任何属性，所以就会找到原型上的getNumber(),所以打印结果为 console.log(3);


第七个问题 new new Yjhl().getNumber() 相当于 new ((new Yjhl()).getNumber)();先初始化Yjhl实例化对象，然后将其原型上的getBNumber函数作为构造函数再次new，所以也打印 console.log(3)。


## es6了解吗,说说你所了解的es6,promise知道吗，promise.all()方法和promise.resolve()方法是干什么用的？

## 如何一次性遍历出对象中所有的键。


## session和cookie的区别?



## $().ready和load比有什么优点．

ready事件在DOM结构绘制完成之后就绘执行。这样能确保就算有大量的媒体文件没加载出来，JS代码一样可以执行。

load事件必须等到网页中所有内容全部加载完毕之后才被执行。如果一个网页中有大量的图片的话，则就会出现这种情况：网页文档已经呈现出来，但由于网页数据还没有完全加载完毕，导致load事件不能够即时被触发。


## <input id="text">,$("#text")和docuemnt.getElementById("text")返回一样吗?

<input id="text">,$("#text")和docuemnt.getElementById("text")返回的不是同一个对象，$("#text")返回的是一个数组，另一个返回的是一个DOM原生对象，转换如下：

```js
  $("#text")[0] == document.getElementById("text")
  $("#text") == $(document.getElementById("text"))
```


## 断点(断言)？

## 使用原声js 实现深拷贝.

## javascript 语言的继承是怎么实现的?

## promise 是什么？

## Tcp 与 udp 协议的区别是？

## settimeOut 与 setmmediate(),process.nextTick() 执行优先级



## Cookie的利弊

cookie能够持久保持客户端的数据,能够分担服务器的压力.
弊端:  数量限制.每个特定的域名下只能最多生成20个cookie, IE7之后, Firefox最多最多50个 chrome和safsri没有硬性限制coolie最大字节为4096, 为了兼容性一般不超过4096个安全性.
被人拦截cookie后可以轻易获取所有session信息有些状态不可能保存在客户端.

每次请求一个页面都会发送cookie, 浪费带宽, 且不可跨域调用.




# 4. React

## React中父子组件的通讯方式？

## 你用react，都用了它的什么功能？

## react的开源协议发生改变，你知道吗？

## react,react-redux等技术链有实际的应用？

## react生命周期，redux的工作原理。

# 5. React Native

## react-native 签名打包,用过的组件,没有写过原生app.

用redux管路状态，登录注册时点击提交，数据保存在哪里，在哪里进行fetch与后台进行交互
mongodb 模板搭建,增删改查方法，修改多个数据(update后面添加{multi:true}),
js 数组去重，可以使用遍历的方法，也可以使用ES6的set数据结构,
js保留小数点后两位,numbers.tofixed(2)



## react native在安卓和IOS的兼容性，安卓支持到哪个版本，面向哪些用户？


# 6. Node.js

## node为什么可以用js?


## nodejs的优缺点?

## restful方面经常使用哪些，分别用来做什么？


## export 和 module.export 区别?



# 7. Mongodb & MySQL

## 问到MongoDB数据库的操作(增删改查)以及其他的方法。

## MySQL数据库中MyISAM与InnoDB两种存储引擎的不同点？


# 8. Pythobn

## 显示目录结构
## Python中的readline返回值是什么?


# 9. 性能优化

## 说一说前端性能优化方法有哪些？



# 10. Other


## 打开网页发生了哪几步行为

输入网址后发生的事件:

在浏览器输入：http://www.baidu.com/，最后，浏览器呈现出相应网页，这个过程究竟发生了什么？

第一步，解析域名，找到主机IP

（1）浏览器会缓存DNS一段时间，一般2-30分钟不等。如果有缓存，直接返回IP，否则下一步。

（2）缓存中无法找到IP，浏览器会进行一个系统调用，查询hosts文件。如果找到，直接返回IP，否则下一步。（在计算机本地目录etc下有一个hosts文件，hosts文件中保存有域名与IP的对应解析，通常也可以修改hosts科学上网或破解软件。）

（3）进行了（1）（2）本地查询无果，只能借助于网络。路由器一般都会有自己的DNS缓存，ISP服务商DNS缓存，这时一般都能够得到相应的IP。如果还是无果，只能借助于DNS递归解析了。

（4）这时，ISP的DNS服务器就会开始从根域名服务器开始递归搜索，从.com顶级域名服务器，到baidu的域名服务器。

到这里，浏览器就获得了IP。在DNS解析过程中，常常会解析出不同的IP。比如，电信的是一个IP，网通的是另一个IP。这是采取了智能DNS的结果，降低运营商间访问延时，在多个运营商设置主机房，就近访问主机。电信用户返回电信主机IP，网通用户返回网通主机IP。当然，劫持DNS，也可以屏蔽掉一部分网点的访问，某防火长城也加入了这一特性。

第二部，浏览器与网站建立TCP连接

浏览器利用IP直接与网站主机通信。浏览器发出TCP（SYN标志位为1）连接请求，主机返回TCP（SYN，ACK标志位均为1）应答报文，浏览器收到应答报文发现ACK标志位为1，表示连接请求确认。浏览器返回TCP（）确认报文，主机收到确认报文，三次握手，TCP链接建立完成。

第三部分，浏览器发起GET请求

浏览器向主机发起一个HTTP-GET方法报文请求。请求中包含访问的URL，也就是http://www.baidu.com/ ，还有User-Agent用户浏览器操作系统信息，编码等。值得一提的是Accep-Encoding和Cookies项。Accept-Encoding一般采用gzip，压缩之后传输html文件。Cookies如果是首次访问，会提示服务器建立用户缓存信息，如果不是，可以利用Cookies对应键值，找到相应缓存，缓存里面存放着用户名，密码和一些用户设置项。

第四部分，显示页面或返回其他

返回状态码200 OK，表示服务器可以相应请求，返回报文，由于在报头中Content-type为“text/html”，浏览器以HTML形式呈现，而不是下载文件。

但是，对于大型网站存在多个主机站点，往往不会直接返回请求页面，而是重定向。返回的状态码就不是200 OK，而是301,302以3开头的重定向码，浏览器在获取了重定向响应后，在响应报文中Location项找到重定向地址，浏览器重新第一步访问即可。

补充一点的就是，重定向是为了负载均衡或者导入流量，提高SEO排名。利用一个前端服务器接受请求，然后负载到不同的主机上，可以大大提高站点的业务并发处理能力；重定向也可将多个域名的访问，集中到一个站点；由于baidu.com，www.baidu.com会被搜索引擎认为是两个网站，照成每个的链接数都会减少从而降低排名，永久重定向会将两个地址关联起来，搜索引擎会认为是同一个网站，从而提高排名。




## 对象上的方法，数组的方法。

## 开发的时候如何检验错误，那么项目上线时如何将打印结果取消，当项目再次开发时如何在将打印显示。




# 11. HR问题


## 都做过什么项目，用什么技术做的？

## 在项目开发中担任什么角色？

## 这个项目上线了吗，有上线的项目吗？

## 为什么来北京发展？

## 可以看看你上线的项目吗？

## 前端开发是用的github吗？使用的是什么代码规范？

## 你有什么问题需要问我？

## 你期望的薪资是多少?

## 问到项目的时候，项目介绍以及技术方面和项目架构。







编写一个函数，参数１为字符串数组arrA,参数２为字符串数组arrB，要求返回字符串数组，其内容是arrA除去arrB之后的数据， 例如：arrA为["abc","123","xyz","miaoqu"],arrB为["xyz","z","123"],则返回结果为["abc","miaoqu"]
中间自适应，两边固定宽度，请写出几种方法　　

有一个div元素，以及按钮A,按钮B和按钮C.点击按钮A，会向地址urlA发出一个Ajax请求，并将返回的字符串填充到div中（覆盖div中原有的数据）; 点击按钮B,会向地址urlB发出一个Ajax请求，并将返回的字符串填充到div中（覆盖div中原有的数据）;点击按钮C亦同． 现在要求用户随意点击按钮，而div中的数据总是显示最后一次点击按钮所请求回来的数据．请问如何设计和编写代码来实现．
