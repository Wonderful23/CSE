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
    1）Vue的组件化开发：将视图中的常用模块封装成一个个组件。而一个网页可以分割成多个可复用的组件，每个组件都可以包含html，css，JavaScript，用于渲染网页的特定部分。类似于面向对象中的类，和面向过程中的函数。
    2）Vue的数据驱动：视图是由数据驱动生成的，对视图的修改不会直接修改DOM，而是修改相应的数据。当交互复杂时，我们只是关心数据的修改，这让代码的逻辑变得清晰，而且由于不触碰到DOM，有利于代码的维护。
    3）Vue的双向绑定：Vue使用的是数据劫持结合发布者-订阅者模式。
    1.需要对observe的数据对象进行递归遍历，包括子属性对象的属性，都加上setter  getter。这个对象的某个属性赋值，就会触发setter，那么就能监听到数据变化。
   2.需要compile解析模板指令，将模板中的变量替换成数据，接着初始化渲染页面视图，并将每个指令对应的节点绑定更新函数，添加监听数据的订阅者。一旦数据有变动，订阅者收到通知，就会更新视图
  接着，Watcher订阅者是Observer和Compile之间通信的桥梁，主要负责：
         1）在自身实例化时，往属性订阅器（Dep）里面添加自己
         2）自身必须有一个update()方法
         3）待属性变动，dep.notice()通知时，就调用自身的update()方法，并触发Compile中绑定的回调
   3.viewmodel(vue实例对象)作为数据绑定的入口，整合Observer、Compile、Watcher三者，通过Observer来监听自己的model数据变化，通过Compile来解析编译模板指令，最终利用Watcher搭起Observer和Compile之间的通信桥梁，达到数据变化 (ViewModel)-》视图更新(view)；视图变化(view)-》数据(ViewModel)变更的双向绑定效果。
  4)Virtual-dom:Virtual Dom可以看做一棵模拟了DOM树的JavaScript树，其主要是通过vnode,实现一个无状态的组件，当组件状态发生更新时，然后触发Virtual Dom数据的变化，然后通过Virtual Dom和真实DOM的比对，再对真实DOM更新。可以简单认为Virtual Dom是真实DOM的缓存。
  我们实现一个具有复杂状态的界面，组件上绑定的数据就会很多。由于界面的状态很多多，我们需要维护的事件和数据就很多。在这种情况下，我们使用virtual DOM只更新状态发生变化的视图。这样不仅有利于性能的提升，而且从移植性上看，Virtual Dom对真实dom做了一次抽象，Virtual Dom对应的可以不是浏览器的DOM，而是不同设备的组件，极大的方便了多平台的使用。
      Virtual-DOM的实现过程:
      1)初始渲染时，首先将数据渲染为 Virtual DOM，然后由 Virtual DOM 生成 DOM。
      2)数据更新时，渲染得到新的 Virtual DOM，与上一次得到的 Virtual DOM 进行 diff，得到所有需要在 DOM 上进行的变更，然后在 patch 过程中应用到 DOM 上实现UI的同步更新。
   5)MVVM模型：(Model-View-ViewModel)
   1.ViewModel 是Vue的核心也是vue的一个实例，可以用于连接View和Model，是一个同步View和model的对象。
   2.DOM Listeners和Data Bindings是实现双向绑定的关键。
   3.DOM Listeners用于监测页面上DOM元素的变化，如果有变化，则更改Model中的数据； 
   4.Data Bindings工具会帮我们更新页面中的DOM元素
   5.View 代表UI 组件，它负责将数据模型转化成UI 展现出来
   6.Model 层代表数据模型，可以在Model中定义数据修改和操作的业务逻辑
   7.Vue是以数据为驱动的，Vue自身将DOM和数据进行绑定，一旦创建绑定，DOM和数据将保持同步，每当数据发生变化，DOM会跟着变化。
   8.在MVVM模式下，View和model不可以直接通信，要应用ViewModel来实现
   MVVM的优点：方便测试：我们可以测试ViewModel来验证我们的代码是否有误。
              独立开发：开发人员可以更加注重业务逻辑和数据开发（ViewModel）设计人员更加注重界面的开发（View）
              低耦合性：View可以独立于Model的修改
              可重用性：可以将视图逻辑封装成一个ViewModel，多个View可以通过ViewModel重复使用这段视图逻辑。
Vue的一些缺点：
    1.Vue诞生的时间较迟，有些地方还不是很成熟。
    2.Vue的社区不大，一旦遇到问题，Vue的解决成本较高。
    3.Vue还不支持一些著名的第三方库。
