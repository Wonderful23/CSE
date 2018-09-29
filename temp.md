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
>>Vue将网页分割成一个个可复用的组件，每个组件由html，Javascript，css封装形成。这些组件用于渲染网页的特定<br></br>部分。类似于面向对象中的类，和面向过程中的函数。<br></br>
>>
![ABD](https://github.com/Wonderful23/-/blob/master/11/v2-bba1a9deb9200210257d250f1cdb9ee3_hd.jpg)
><b>Vue的数据驱动</b>
>>视图是由数据驱动生成的，对视图的修改不会直接修改DOM，而是修改相应的数据。当交互复杂时，我们只是关<br></br>心数据的修改，这让代码的逻辑变得清晰，而且由于不触碰到DOM，有利于代码的维护。
>>
><b>Vue的双向绑定</b>
>>Vue使用的是数据劫持结合发布者-订阅者模式。
>>> * 需要对observe的数据对象进行递归遍历，包括子属性对象的属性，都加上setter  getter。这个对象的某<br></br>个属性赋值，就会触发setter，那么就能监听到数据变化。<br></br>
>>>* 需要compile解析模板指令，将模板中的变量替换成数据，接着初始化渲染页面视图，并将每个指令对应<br></br>的节点绑定更新函数，添加监听数据的订阅者。一旦数据有变动，订阅者收到通知，就会更新视图<br></br>
>>> * Watcher订阅者是Observer和Compile之间通信的桥梁，主要负责：
>>>> * 在自身实例化时，往属性订阅器（Dep）里面添加自己<br></br>
>>>> * 自身必须有一个update()方法<br></br>
>>>> * 待属性变动，dep.notice()通知时，就调用自身的update()方法，并触发Compile中绑定的回调
>>>    * viewmodel(vue实例对象)作为数据绑定的入口，整合Observer、Compile、Watcher三者，通过Observer<br></br>来监听自己的model数据变化，通过Compile来解析编译模板指令，最终利用Watcher搭起Observer和<br></br>Compile之间的通信桥梁，达到数据变化(ViewModel)-》视图更新(view)；视图变化(view)-》数据<br></br>(ViewModel)变更的双向绑定效果。
>>>
>>
>
<br>/<br>
![ABD](https://github.com/Wonderful23/-/blob/master/11/%E6%A8%A1%E5%9E%8B.jpg)
><b>Virtual-DOM</b>
>>Virtual Dom可以看做一棵模拟了DOM树的JavaScript树，其主要是通过vnode,实现一个无状态的组件，当组件状态<br></br>发生更新时，然后触发Virtual Dom数据的变化，然后通过Virtual Dom和真实DOM的比对，再对真实DOM更新。<br></br>可以简单认为Virtual Dom是真实DOM的缓存。<br></br>
我们实现一个具有复杂状态的界面，组件上绑定的数据就会很多。由于界面的状态很多多，我们需要维护的事件和<br></br>数据就很多。在这种情况下，我们使用virtual DOM只更新状态发生变化的视图。这样不仅有利于性能的提升，而<br></br>且从移植性上看，Virtual Dom对真实dom做了一次抽象，Virtual Dom对应的可以不是浏览器的DOM，而是不同设<br></br>备的组件，极大的方便了多平台的使用。
>> Virtual-DOM的实现过程
>>> * 初始渲染时，首先将数据渲染为 Virtual DOM，然后由 Virtual DOM 生成 DOM。<br></br>
>>> * 数据更新时，渲染得到新的 Virtual DOM，与上一次得到的 Virtual DOM 进行 diff，得到所有需要在 <br></br>DOM 上进行的变更，然后在 patch 过程中应用到 DOM 上实现UI的同步更新。
>>>
>>
>
![ABD](https://github.com/Wonderful23/-/blob/master/11/%E6%A8%A1%E5%9E%8B.jpg)
