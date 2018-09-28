1.背景：随着网页更加动态化，功能更加复杂，很多传统的服务端的代码被引入到浏览器中，这就导致了网页中的JS代码的数量急剧增多。JavaScript代码连接了很多html和css代码，如果缺乏正规的组织形式，就会对网页的编写和维护产生影响。在此前提下，就产生了很多的JavaScript Framework。Vue 无疑是其中最出色的框架之一。
2.简介：Vue是一套构建用户界面的渐进式框架。Vue被设计成自底向上的逐层应用。Vue的核心库只关注视图层面，不仅容易上手，还便于与第三方库，已有项目相结合。
3.名词解释：渐进式框架：1）声明式渲染：采用简洁的模板语法将数据声明式的渲染进入DOM中比如借助v-model="message"和{{message}}将message渲染进入DOM中。
                      2）组件系统：自定义一些元素，构成组件，类似于C++中的class
                      3）客户端路由：借助Vue插件vue-router向每个路由发出渲染的组件类型、渲染的地址的信息。
                      4）状态管理:借助Vue的状态管理插件管理了所有组件的状态。
                      5）构建系统:借助Vue-ci构建大型应用,进行前后端分离、优化代码结构、提高开发效率。
                      Vue的渐进式框架的应用：1.用于将Vue作为应用的一部分嵌入现有的服务端应用程序，提高交互式体验
                                           2.将更多业务逻辑放在前端实现
                      工具：Vue核心库+Vue的生态系统。
4.Vue的特点：
    1）Vue的组件化开发
