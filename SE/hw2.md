![ABD](http://image.woshipm.com/wp-files/2014/12/907f2ff9d9f3a8c202d3dd210a10c8b3.png)<br></br>
<t></t> Web APP & Native APP & Hybrid APP
===================================================
# Web APP
## Web APP 简介
> Web APP是基于Web系统，通过html5实现的存在于浏览器中的应用程序。Web APP 无需下载安装就，类似于我们所提的轻应用。
## Web APP 优点：
-  开发成本低

- 更新快

- 无需手动更新升级

- 可以跨多个平台和终端使用
## Web App 缺点：
- 对网络环境依赖性较大：当遇到网速慢，网络不稳定是，用户请求页面的效率就会下降，给用户带来不好的体验。<br></br>
- H5技术自身渲染性能较弱：对复杂的图形样式，多样的动效，自定义额字体等支持性不强。<br></br>
- 无法获得系统级别的通知和动效：由于html5语言的技术特性，无法调用系统级别的权限，例如系统级别的弹窗，通知，地理信息，通讯录，语音。<br></br>
- 交互设计受限多：影响一些页面场景和逻辑的理解，导航不明显，原有的底部导航缺失，更小的页面空间（浏览器页面本身占用一部分屏幕），更大的信息记忆负担

# Native APP
## Native APP 简介
>简介：native APP 是一种基于智能手机操作系统Android iOS，WP并使用原生程式编写运行的第三方应用程序，也叫作本地APP。与web app 相反，native app 能够使用手机硬件功能，如扬声器，加速度传感器，摄像头等。
## Native APP 优点：
- 打造完美的用户体验

- 性能稳定

- 操作速度快，使用起来体验感好

- 可以访问本地资源

- 交互式设计更加流畅

- 拥有系统级别的通知和提醒

- 用户留存率高
## Native APP 缺点：
- 移植到不同平台上较麻烦，需要开发多平台版本

- 维护成本高：除了需要维护最新版本，还需维护先前推出的版本

- 用户必须手动下载更新，到最新版本

- 更新较为缓慢，需要通过store和market的确认，审核流程较为复杂。
# Hybrid APP
## Hybrid APP 简介：
>引用外国人的定义：<br></br>
    Hybrid App:Hybrid App is a mobile application that is coded in both browser-supported language and computer language. They are         available through application distribution platforms such as the Apple App Store, Google Play etc. Usually, they are downloaded         from the platform to a target device, such as iPhone, Android phone or Windows Phone. The subscribers need to install to run           then<br></br>
>简而言之，Hybrid App(混合模式移动应用)是指介于web-app、native-app这两者之间的app，兼具"Native App良好用户交互体验的优势"和"Web App跨平台开发的优势"。它虽然看上去是一个Native App，但只有一个UI WebView，里面访问的是一个Web App。
## 几种类型的hybrid APP
- <b>多View混合型</b>
>即Native View和Web View独立展示，交替出现。这种应用混合逻辑相对简单。即在需要的时候，将WebView当成一个独立的View(Activity)运行起来，在WebView内完成相关的展示操作。这种移动应用主体通常是Native App，Web技术只是起到补充作用。开发难度和Native App基本相当。
- <b>单View混合型</b>
>即在同一个View内，同时包括Native View和Web View。互相之间是覆盖(层叠)的关系。这种Hybrid App的开发成本较高，开发难度较大，但是体验较好。
- <b>Web主体型</b>
>即移动应用的主体是Web View，主要以网页语言编写，穿插Native功能的Hybrid App开发类型。这种类型开发的移动应用体验相对而言存在缺陷，但整体开发难度大幅降低，并且基本可以实现跨平台。
## Hybrid APP 优点：
- 结合了Native APP和web技术，可以轻松使用跨平台web技术，也可以在需要的时候直接访问native API，兼具"Native App良好用户交互体验的优势"和"Web App跨平台开发的优势"。

- Native代码部分使用操作系统的API来创建嵌入式HTML渲染引擎，为此其成为浏览器和设备的API之间的桥梁，帮助开发者充分利用移动设备的全部特性。

- App开发者可以选择编写自己的桥梁，或者充分利用现成的解决方案。
## Hybrid APP缺点：
- 采用融合native和Web的方法摈弃了任何离线可用性，因为设备与网络没有连接时，无法访问设备

- 把Web代码封装到APP里面可以提高性能和可访问性，但是不允许远程更新
# Web APP & Hybrid APP & Native APP 比较
![ABD](http://image.woshipm.com/wp-files/2014/12/b0cf05c189c1814380709ec94ebd5a7b.png)
# Reference
[三种APP的优缺点比较](http://www.woshipm.com/pd/123646.html)
