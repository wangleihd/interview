一.
  react-native 签名打包,用过的组件,没有写过原生app
      用redux管路状态，登录注册时点击提交，数据保存在哪里，在哪里进行fetch与后台进行交互
  mongodb 模板搭建,增删改查方法，修改多个数据(update后面添加{multi:true}),
  js 数组去重，可以使用遍历的方法，也可以使用ES6的set数据结构,
  js保留小数点后两位,numbers.tofixed(2)


二.　盈嘉互联　　笔试+面试
  1.doctype中HTML和XHTML的区别：
    XHTML严格规范标签大小写，属性值加引号等等，用来规范语法
    HTML是一种基本的WEB网页设计语言，XHTML是一个基于XML的置标语言
    最主要的不同：
      XHTML 元素必须被正确地嵌套。
      XHTML 元素必须被关闭。
      标签名必须用小写字母。
      XHTML 文档必须拥有根元素。

  2.行内元素：span a img input i u b strong del ins
    块级元素: div p h1-h6 ul li ol

  3.标签选择器 类选择器 id选择器 通配选择器
    优先级：!important > style(行内样式) > id > class > 标签　> 继承 > 浏览器默认

  4.div垂直居中的方法
    一个父div设置相对定位 relative，
    一个子div设置绝对定位 absolute，left,top都为50%,不知道自身宽高时可以用
    transform:translate(-50%,50%);
    知道宽高时可以用margin-left:-selfwidth*50%;margin-top:-selfheight*50%;

  5.<input id="text">,$("#text")和docuemnt.getElementById("text")返回的不是同一个对象，$("#text")返回的是一个数组，另一个返回的是一个DOM原生对象，转换如下：
    $("#text")[0] == document.getElementById("text")
    $("#text") == $(document.getElementById("text"))

  6.事件委托,举例说明事件委托
    使用事件委托技术能让你避免对特定的每个节点添加事件监听器；相反，事件监听器是被添加到它们的父元素上。事件监听器会分析从子元素冒泡上来的事件，找到是哪个子元素的事件。父元素上注册事件的回调函数的形参event.target就可以找到真正触发事件的子元素

  7.写一个简单的闭包，说说对闭包的理解
    function closure(){
      var a = 10;
      return function(){
        console.log(a)
      }
    }
    var win = closure();
    win();
    闭包就是有权访问另一个函数作用域中的私有变量的函数

  8.$().ready和load比有什么优点．
    ready事件在DOM结构绘制完成之后就绘执行。这样能确保就算有大量的媒体文件没加载出来，JS代码一样可以执行。
    load事件必须等到网页中所有内容全部加载完毕之后才被执行。如果一个网页中有大量的图片的话，则就会出现这种情况：网页文档已经呈现出来，但由于网页数据还没有完全加载完毕，导致load事件不能够即时被触发。

三.　炎黄新星　　笔试+上机
  1.用ajax发送请求数据 {name:"lisi"},成功打印name的值,失败打印请求失败
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

  2.ajax跨域的方式有哪几种？
    jsonp  cors  websocket

  3.http的状态码．
    1xx:  Informational(信息状态码)　　   接受的请求正在处理
    2xx:  Success(成功状态码)　　　　　    请求正常处理完
    3xx:  Redirection(重定向状态码)       需要进行附加操作以完成请求
    4xx:  Client Error(客户端错误状态码)   服务器无法处理请求
    5xx:  Server Error(服务器错误状态码)　　服务器处理请求出错

  4.get和post的区别

  5.HTML5中的存储方式
    cookies
    localStorage
    sessionStorage

  6.es5模拟生成一个类 Person,有两个属性v1,v2,两个方法f1,f2;
      function Person(){
        this.v1 = "v1";
        this.v2 = "v2";
        this.f1 = function(){}
        this.f2 = function(){}
      }

  7.es6生成一个类 Person,有两个属性v1,v2,两个方法f1,f2;
    class Person(){
      construct(v1,v2){
        this.v1 = v1
        this.v2 = v2
      }
      f1(){}
      f2(){}
    }

四．环球优学　　笔试+面试
  1. 二.12
  2. 二.15
  3. 写一个js数组去重方法


五. 国广中播
1.响应式布局:
2.什么是闭包,闭包的优点,闭包跟匿名函数的区别,
3.base64
4.utf-8和unicode的区别
5.ajax
6.跨域
7.session和cookie的区别
8.readline返回值
9.显示目录结构
10.node为什么可以用js



面试单位：妙趣横生（web前端）

地址：北京市朝阳区来广营

面试流程：先做笔试题，之后面的的技术

笔试题

编写一个函数，参数１为字符串数组arrA,参数２为字符串数组arrB，要求返回字符串数组，其内容是arrA除去arrB之后的数据， 例如：arrA为["abc","123","xyz","miaoqu"],arrB为["xyz","z","123"],则返回结果为["abc","miaoqu"]
中间自适应，两边固定宽度，请写出几种方法　　

有一个div元素，以及按钮A,按钮B和按钮C.点击按钮A，会向地址urlA发出一个Ajax请求，并将返回的字符串填充到div中（覆盖div中原有的数据）; 点击按钮B,会向地址urlB发出一个Ajax请求，并将返回的字符串填充到div中（覆盖div中原有的数据）;点击按钮C亦同． 现在要求用户随意点击按钮，而div中的数据总是显示最后一次点击按钮所请求回来的数据．请问如何设计和编写代码来实现．

面试技术

讲讲笔试题第一题的解决思路！

说一说第三题的题意和解决思路！

es6了解吗,说说你所了解的es6,promise知道吗，promise.all()方法和promise.resolve()方法是干什么用的？

fetch()方法干什么用的，是否对该方法进行了封装？发生错误是怎么处理的？

期望薪资是多少？

面试单位：易鑫集团，看看二手车（前端开发工程师）

地址：北京市朝阳区黄衫木店路９号绿森时代广场９层

面试流程：先填表，再面技术，最后是HR

填表

主要是个人信息及教育背景，家庭情况，工作过的公司名称和时间以及联系人电话

面试技术

都做过什么项目，用什么技术做的？

在项目开发中担任什么角色？

这个项目上线了吗，有上线的项目吗？

react native在安卓和IOS的兼容性，安卓支持到哪个版本，面向哪些用户？

为什么来北京发展？

可以看看你上线的项目吗？

为什么要用fetch(),他有什么优势？

你用react，都用了它的什么功能？

这个项目用什么编译的？

前端开发主要配套的库和模块？

react的开源协议发生改变，你知道吗？

react,react-redux等技术链有实际的应用？

前端开发是用的github吗？使用的是什么代码规范？

HR面试

你有什么问题需要问我？

你期望的薪资是多少?

面试单位：况客科技（前端开发工程师）

地址：北京 - 朝阳区 - 朝阳门 - 吉庆里14号佳汇国际中心A座1503室

面试流程：先填表，再面技术(一遍看题一遍说思路)

填表

主要是个人信息及教育背景，家庭情况，工作过的公司名称和时间以及联系人电话

技术面试(边看题边说实路)

js的数据类型有哪些？哪些是原生数据类型？哪些是引用数据类型？
什么是作用域链？什么是原型链？什么是闭包？
ES6的新特性有哪些？
动手实现Array.prptotype.sort()方法，即数组排序？
React中父子组件的通讯方式？
说一说前端性能优化方法有哪些？


1.问到项目的时候，项目介绍以及技术方面和项目架构。
2.问到MongoDB数据库的操作(增删改查)以及其他的方法。
3.restfor方面经常使用哪些，分别用来做什么？
4.react生命周期，redux的工作原理。
5.JS中，如何保留小数点后两位。
6.es6中常用的数据结构，特意说了map，还问了数组去重(set方法)。
7.如何一次性遍历出对象中所有的键。
8.对象上的方法，数组的方法。
9.开发的时候如何检验错误，那么项目上线时如何将打印结果取消，当项目再次开发时如何在将打印显示。
10.断点(断言)？


2017.10.16 上午
hr 面试 
红科网安  
介绍一下你的项目
nodejs的优缺点
为什么离职

2017.10.17 下午
面试

笔试
1.es6 实现链表数据结构，具有append(),insert(),remove()方法
2.express 和 module.express 区别
3. 使用原声js 实现深拷贝
4. 编写一个比包的实例
5. javascript 语言的继承是怎么实现的
6.promise 是什么？
7.Tcp 与 udp 协议的区别是？
8.Nodejs未知错误处理
9.settimeOut 与 setmmediate(),process.nextTick() 执行优先级

