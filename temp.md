![ABD](https://github.com/Wonderful23/-/blob/master/11/t013dad0e25dfb0b247.jpg)
<t></t>PROS & CONS OF Vue.JS
================================
# Vue的简介
>Vue是一套构建用户界面的<b>渐进式框架</b>。Vue被设计成<b>自底向上</b>的逐层应用。Vue的核心库只关注视图层面，不仅容易上<br></br>手，还便于与第三方库，已有项目相结合。
# Vue出现的背景
>随着网页更加动态化，功能更加复杂，很多传统的服务端的代码被引入到浏览器中，这就导致了网页中的JS代码的数量<br></br>急剧增多。JavaScript代码连接了很多html和css代码，如果缺乏正规的组织形式，就会对网页的编写和维护产生影响。在<br></br>此前提下，就产生了很多的JavaScript Framework。Vue 无疑是其中最出色的框架之一。
# Vue的几个突出特点 
### 1.Vue采用渐进式框架
>渐进式（引用大神的解释）
>>Vue (pronounced /vjuː/, like view) is a progressive framework for building user interfaces. Unlike other monolithic frameworks, Vue is designed from the ground up to be incrementally adoptable. The core library is focused on the view layer only, and is very easy to pick up and integrate with other libraries or existing projects. On the other hand, Vue is also perfectly capable of powering sophisticated Single-Page Applications when used in combination with modern tooling and supporting libraries.
>>
><b>渐进式框架</b>（见下图）
<br></br>
![ABD](https://github.com/Wonderful23/-/blob/master/11/%E6%B8%90%E8%BF%9B%E5%BC%8F2.png)
><b>框架解释</b>：
>>1）声明式渲染：采用简洁的模板语法将数据声明式的渲染进入DOM中比如借助v-model="message"和{{message}}将message渲染进入DOM中。
<br></br>2）组件系统：自定义一些元素，构成组件，类似于C++中的class
<br></br>3）客户端路由：借助Vue插件vue-router向每个路由发出渲染的组件类型、渲染的地址的信息。
<br></br>4）状态管理:借助Vue的状态管理插件管理了所有组件的状态。
<br></br>5）构建系统:借助Vue-ci构建大型应用,进行前后端分离、优化代码结构、提高开发效率。
>>
><b>Vue的渐进式框架在工程的应用</b>：
>>1)将Vue作为应用的一部分嵌入现有的服务端应用程序，提高交互式体验<br></br>
2)将更多业务逻辑放在前端实现
>>
![ABD](https://github.com/Wonderful23/-/blob/master/11/%E6%B8%90%E8%BF%9B%E5%BC%8F.png)
><b>Vue的组件化开发</b>
>>将视图中的常用模块封装成一个个组件。而一个网页可以分割成多个可复用的组件，每个组件都可以包含html，css，JavaScript，用于渲染网页的特定部分。类似于面向对象中的类，和面向过程中的函数。
>>
![ABD](https://github.com/Wonderful23/-/blob/master/11/%E6%B8%90%E8%BF%9B%E5%BC%8F.png)
