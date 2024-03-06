---
title: 面试——其他篇
date: 2020-12-29 10:23:51
tags: 
  - 面试
  - js
type: 面试                                                                 # 标签、分类
description:  JavaScript（简称“JS”） 是一种具有函数优先的轻量级，解释型或即时编译型的编程语言。
top_img: https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=955487690,3458128037&fm=26&gp=0.jpg             # 文章的顶部图片
aside: true                                                                         # 展示文章侧边栏(默认为true)
categories: 
  - 面试
  - js                                                                 # 文章标签
cover: https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=955487690,3458128037&fm=26&gp=0.jpg                 # 文章的缩略图（用在首页）
---

# 询问工作经历，在项目中如何做性能优化的？
  1. content方面
    * 减少HTTP请求：合并文件、CSS精灵、inline Image
    * 减少DNS查询：DNS查询完成之前浏览器不能从这个主机下载任何任何文件。方法：DNS缓存、将资源分布到恰当数量的主机名，平衡并行下载和DNS查询
    * 避免重定向：多余的中间访问
    * 使Ajax可缓存
    * 非必须组件延迟加载
    * 未来所需组件预加载
    * 减少DOM元素数量
    * 将资源放到不同的域下：浏览器同时从一个域下载资源的数目有限，增加域可以提高并行下载量
    * 减少iframe数量
    * 不要404

  2. Server方面
    * 使用CDN
    * 添加Expires或者Cache-Control响应头
    * 对组件使用Gzip压缩
    * 配置ETag
    * Flush Buffer Early
    * Ajax使用GET进行请求
    * 避免空src的img标签

  3. Cookie方面
    * 减小cookie大小
    * 引入资源的域名不要包含cookie

  4. css方面
    * 将样式表放到页面顶部
    * 不使用CSS表达式
    * 使用不使用@import
    * 不使用IE的Filter

  5. Javascript方面
    * 将脚本放到页面底部
    * 将javascript和css从外部引入
    * 压缩javascript和css
    * 删除不需要的脚本

  6. 图片方面
    * 优化图片：根据实际颜色需要选择色深、压缩
    * 优化css精灵
    * 不要在HTML中拉伸图片
    * 保证favicon.ico小并且可缓存
---

# 浏览器http请求过多怎么解决？
  1. 合并JS、CSS文件 
  2. 合并图片css sprite 
  3. 使用 Image maps 
  4. 4data嵌入图片：如base64 
  5. 使用CDN，减少http请求头 Web安全
---

# 组件库如何做按需加载
---

# 聊项目：为什么做，功能是什么，你做了什么，难点是什么，怎么解决的，结果怎么样
---

# 跨平台的框架用过哪些，这些框架的好处是什么，问题是什么，各自的区别是什么
---

# 你觉得做前端工程师需要什么能力
---

# 你对前端未来的发展趋势的看法
---

# 你认为自己做的项目有什么值得的说道的地方吗？这里其实就是考察项目的亮点，可以说一些项目难点是如何解决的，或者介绍一些项目中用到的比较高级的技术。
---

# 常使用的库有哪些？常用的前端开发工具？开发过什么应用或组件？
---

# 除了前端以外还了解什么其它技术么？你最最厉害的技能是什么？
---

# 如何管理前端团队?
---

# 你在现在的团队处于什么样的角色，起到了什么明显的作用？
---

# 最近在学什么？能谈谈你未来3，5年给自己的规划吗？
---

# 简单描述一下你做过的移动APP项目研发流程？
---

# 你对加班的看法？
---

# 你的优点是什么？缺点是什么？
---

#  在项目中所承担的角色，怎样看待自己的角色
---

# 自己有什么技术上的优势
---

# 职业规划
---

# 工作之余，平时都做些什么
---

#  未来3年的打算？
---

# 你期望的团队和工作是什么样的？
---

# 说说你对中台的理解，和后台有什么区别
---

# 如果团队成员因某种原因没有完成相应的任务，该怎么办
---

# 平时如何管理你的项目？
  1. 先期团队必须确定好全局样式（globe.css），编码模式(utf-8) 等；
  2. 编写习惯必须一致（例如都是采用继承式的写法，单样式都写成一行）；
  3. 标注样式编写人，各模块都及时标注（标注关键样式调用的地方）；
  4. 页面进行标注（例如 页面 模块 开始和结束）；
  5. CSS跟HTML 分文件夹并行存放，命名都得统一（例如style.css）；
  6. JS 分文件夹存放 命名以该JS功能为准的英文翻译。
  7. 图片采用整合的 images.png png8 格式文件使用 尽量整合在一起使用方便将来的管理 
---

# 对前端界面工程师这个职位是怎么样理解的？它的前景会怎么样？
    <1>.前端是最贴近用户的程序员，比后端、数据库、产品经理、运营、安全都近。
    	1)、实现界面交互
    	2)、提升用户体验
    	3)、有了Node.js，前端可以实现服务端的一些事情

    <2>.前端是最贴近用户的程序员，前端的能力就是能让产品从 90分进化到 100 分，甚至更好，

    <3>.参与项目，快速高质量完成实现效果图，精确到1px；

    <4>.与团队成员，UI设计，产品经理的沟通；

    <5>.做好的页面结构，页面重构和用户体验；

    <6>.处理hack，兼容、写出优美的代码格式；

    <7>.针对服务器的优化、拥抱最新前端技术。
---

# 有学习什么前端前沿的技术吗？canvas了解过吗？WebGL呢？
  * WebGL: WebGL (Web图形库) 是一种JavaScript API，用于在任何兼容的Web浏览器中呈现交互式3D和2D图形，而无需使用插件。WebGL通过引入一个与OpenGL ES 2.0紧密相符合的API，可以在HTML5 元素中使用。
---

# 权限系统是怎么设计的
  1. 前端控制： 前端的控制比较简单，从后台获取到用户的权限之后，可以存在session或者cookie中，然后在页面加载的时候，通过session或者cookie中存的权限来选择让该功能展现或者禁用。
  2. 后台控制： 仅仅依靠前端的控制是无法完美解决权限控制的问题，因为前端页面的加载过程是在浏览器中完成的，用户可以自行篡改页面；或者用户可以直接通过URI请求来获取非法权限功能。所以需要在后台实现权限控制。
  3. 全局异常管理： 思路是在拦截器中权限校验失败时，抛出一个权限校验失败的异常，然后通过全局异常管理类来捕获并返回前端特定的格式。具体如下。
---

# 假如进入一个页面没有权限进入，如何判断
大意在前端处理分为路由和接口两个方面，路由在vue-route中的钩子函数beforeEach，接口是通过axios响应拦截器处理
---

# 谈谈以前端角度出发做好SEO需要考虑什么？
  1. 了解搜索引擎如何抓取网页和如何索引网页:  你需要知道一些搜索引擎的基本工作原理，各个搜索引擎之间的区别，搜索机器人（SE robot 或叫 web crawler）如何进行工作，搜索引擎如何对搜索结果进行排序等等。
  2. Meta标签优化: 主要包括主题（Title)，网站描述(Description)，和关键词（Keywords）。还有一些其它的隐藏文字比如Author（作者），Category（目录），Language（编码语种）等。
  3. 如何选取关键词并在网页中放置关键词:  首先要给网站确定主关键词（一般在5个上下），然后针对这些关键词进行优化，包括关键词密度（Density），相关度（Relavancy），突出性（Prominency）等等
  4. 了解主要的搜索引擎： 不同的搜索引擎对页面的抓取和索引、排序的规则都不一样。还要了解各搜索门户和搜索引擎之间的关系，比如AOL网页搜索用的是Google的搜索技术，MSN用的是Bing的技术。
  5. 主要的互联网目录
  6. 按点击付费的搜索引擎
  7. 链接交换和链接广泛度
  8. 合理的标签使用
---

# WEB应用从服务器主动推送Data到客户端有那些方式？
  1. html5 websoket
  2. WebSocket通过Flash
  3. XHR长时间连接
  4. XHR Multipart Streaming
  5. 不可见的Iframe
  6. `<script>`标签的长时间连接(可跨域)
---

# 描述几种服务器和客户端之间的通信方式。描述一些网络协议是工作的
同上
---

# 移动端的点击事件的有延迟，时间是多久，为什么会有？ 怎么解决这个延时？
  300ms
---

# 什么是CDN缓存
  * CDN 是一种部署策略，根据不同的地区部署类似nginx 这种服务服务，会缓存静态资源。前端在项目优化的时候，习惯在讲台资源上加上一个 hash 值，每次更新的时候去改变这个 hash，hash 值变化的时候，服务会去重新取资源
  * (CDN)是一个经策略性部署的整体系统，包括分布式存储、负载均衡、网络请求的重定向和内容管理4个要件
---

# cdn用的是哪一种缓存？
---

# 使用CDN有什么好处
  * 使用CDN可以给你的网站加速，本身不影响SEO正常收录和网站优化，相反，还能提升你的网站用户体验，隐藏你的源站IP防止被黑客攻击；
---

# cdn原理
  * 简单概括就是负载均衡，缓存，dns解析
  * 通过dns解析到全局负载均衡服务器，然后再到区域的负载均衡，之后根据一些条件来找合适的缓存服务器，如果第一次访问就从源站拿过来缓存。需要注意的是一切都是根据请求的ip来的，如果ip不合理，那么可能起不到加速效果。缓存和负载均衡的思想在减轻服务器压力方面其实是很常见的
---

# CDN什么资源都能存吗？
  * 不是。
  * CDN 可以存储网站的静态资源，如图片、视频、音频、CSS、JS 等文件。这些文件的特点是文件体积大，访问频率高，但更新不频繁。将这些静态资源缓存到 CDN 上可以降低网站的负载，提高网站的访问速度和用户体验。
  * CDN 不能存储动态数据，如网站的数据库内容、网站程序源代码、用户上传的文件等。这些数据的特点是更新频繁，无法通过 CDN 缓存实现加速。另外，由于 CDN 缓存是公开的，存储敏感数据存在安全隐患。
---

# Cdn有哪些优化静态资源加载速度的方法？
  * 资源调度：CDN会根据用户接入网络的ip寻找距离用户最优路径的服务器。调度的方式主要有DNS调度、http 302调度、使用 HTTP 进行的 DNS 调度（多用于移动端）； 
  * 缓存策略和数据检索：CDN服务器使用高效的算法和数据结构，快速的检索资源和更新读取缓存； 
  * 网络优化：从OSI七层模型进行优化，达到网络优化的目的。 L1物理层：硬件设备升级提高速度 L2数据链路层：寻找更快的网络节点、确保 Lastmile 尽量短 L3路由层：路径优化，寻找两点间最优路径 L4传输层：协议TCP优化，保持长连接、TCP快速打开 L7应用层：静态资源压缩、请求合并
---

# 应当什么场景下实用CDN服务器？
> 我们应该在网站流量大、需要提供多媒体内容服务、需要防止网络安全问题以及电商平台需要进行大促活动等场景下考虑使用CDN。通过CDN的加速和优化，可以提高网站的性能和用户体验，提升网站的竞争力。
---

# JWT的优缺点, 使用场景?
  * 优点:
    - 可扩展性好：应用程序分布式部署的情况下，session需要做多机数据共享，通常可以存在数据库或者redis里面。而jwt不需要。

    - 无状态: jwt不在服务端存储任何状态。jwt可以存储一些常用信息, 有效地使用 JWT，可以降低服务器查询数据库的次数。

  * 缺点:
   	- 安全性： 由于jwt的payload是使用base64编码的，并没有加密，因此jwt中不能存储敏感数据。而session的信息是存在服务端的，相对来说更安全。

   	- 性能：
   	jwt太长。由于是无状态使用JWT，所有的数据都被放到JWT里，如果还要进行一些数据交换，那载荷会更大，经过编码之后导致jwt非常长，cookie的限制大小一般是4k，cookie很可能放不下，所以jwt一般放在local storage里面。并且用户在系统中的每一次http请求都会把jwt携带在Header里面，http请求的Header可能比Body还要大。而sessionId只是很短的一个字符串，因此使用jwt的http请求比使用session的开销大得多。

   	- 一次性： 无状态是jwt的特点，但也导致了这个问题，jwt是一次性的。想修改里面的内容，就必须签发一个新的jwt。

  * 场景:
	  - 有效期短

	  - 只希望被使用一次。jwt具有一次性的特性。单点登录和会话管理非常不适合用jwt，如果在服务端部署额外的逻辑存储jwt的状态，那还不如使用session。
---

# 从浏览器地址栏输入url到显示页面的步骤(以HTTP为例)
  1. 输入网址；
  2. 发送到DNS服务器，并获取域名对应的web服务器对应的ip地址；
  3. 与web服务器建立TCP连接；
  4. 浏览器向web服务器发送http请求；
  5. web服务器响应请求，并返回指定url的数据（或错误信息，或重定向的新的url地址）；
  6. 浏览器下载web服务器返回的数据及解析html源文件；
  7. 生成DOM树，解析css和js，渲染页面，直至显示完成；
---

# 从接口请求到后端响应经过了什么
---

# dns查询过程，使用的协议
  1. 用户主机上运行着DNS的客户端，就是我们的PC机或者手机客户端运行着DNS客户端了
  2. 浏览器将接收到的url中抽取出域名字段，就是访问的主机名，比如http://www.baidu.com/
  3. DNS客户机端向DNS服务器端发送一份查询报文，报文中包含着要访问的主机名字段（中间包括一些列缓存查询以及分布式DNS集群的工作）
  4. 该DNS客户机最终会收到一份回答报文，其中包含有该主机名对应的IP地址
  5. 一旦该浏览器收到来自DNS的IP地址，就可以向该IP地址定位的HTTP服务器发起TCP连接
---

# DNS解析的内部原理
  > DNS通过域名解析系统解析找到了对应的IP地址，域
---

# dns劫持了解吗
---

# HTTP request报文结构是怎样的
  * 首行是Request-Line包括：请求方法，请求URI，协议版本，CRLF
  * 首行之后是若干行请求头，包括general-header，request-header或者entity-header，每个一行以CRLF结束
  * 请求头和消息实体之间有一个CRLF分隔
  * 根据实际请求需要可能包含一个消息实体
---

# HTTP response报文结构是怎样的
  * 首行是状态行包括：HTTP版本，状态码，状态描述，后面跟一个CRLF
  * 首行之后是若干行响应头，包括：通用头部，响应头部，实体头部
  * 响应头部和响应实体之间用一个CRLF空行分隔
  * 最后是一个可能的消息实体
---

# http报文头部有哪些字段?有什么意义?
> 请求头
  1. Accept: 客户端希望获得资源的类型。类似 text/html 则是 MIME 类型，接在后面的 q 代表的是优先级，q 的范围通常在 0 到 1，越大优先级越高。
  2. Accept-Encoding: 客户端支持的压缩算法。服务端可以根据它来使用压缩算法来压缩资源，降低带宽，让用户能更快加载资源。
  3. Accept-Language: 客户端支持的语言。服务端可以通过这个字段来做 国际化，根据用户设置的语言来返回不同国家文案内容。
  4. Host: 当前请求的域名。服务端可以根据这个字段来做 反向代理。
  5. Connection: 客户端是否希望使用 TCP 长连接。
  6. User-Agent: 用户代理。该字段标注了发送方的一些信息，你可以通过它来知道请求方是浏览器、爬虫、postman 还是 cURL。
> 响应头：
  1. Content-Type：服务端返回的资源类型，可以带上使用的编码格式。
  2. Content-Encoding：返回资源使用的压缩格式。
  3. Content-Length： HTTP 消息体的长度。
  4. Date：HTTP 响应报文生成的时间，使用了 GMT 格式。
  5. Connection：服务端决定使用长连接还是短连接。
  6. Server：使用了哪种服务器。
---

# 和浏览器缓存相关的HTTP头有哪些
> 请求头：
  1. Cache-Control
  2. Pragma
  3. If-Modified-Since
  4. If-None-Match
> 响应头：
  1. Last-Modified
  2. ETag
---

# http状态码有那些？分别代表是什么意思？
  * 100-199 用于指定客户端应相应的某些动作。 
  * 200-299 用于表示请求成功。 
  * 300-399 用于已经移动的文件并且常被包含在定位头信息中指定新的地址信息。 
  * 400-499 用于指出客户端的错误。400    1、语义有误，当前请求无法被服务器理解。401   当前请求需要用户验证 403  服务器已经理解请求，但是拒绝执行它。
  * 500-599 用于支持服务器错误。 503 – 服务不可用
---

# 一个http的报文的头和body之间有什么分隔
> HTTP协议规定,HTTP首部(headers)和HTTP主体之间是以一个空行分割的
---

# http协议中301和302的区别
  * 302重定向是暂时的重定向，搜索引擎会抓取新的内容而保存旧的网址。由于效劳器前往302代码，搜索引擎以为新的网址只是暂时的。
  * 301重定向是永久的重定向，搜索引擎在抓取新内容的同时也将旧的网址交换为重定向之后的网址。
---

# 介绍HTTP2.0，具体是怎么实现头部压缩的呢？多路复用的过程又是怎么样的呢？
---

# 介绍下304过程。(原理)
  1. 服务器首先产生ETag，服务器可在稍后使用它来判断页面是否已经被修改。本质上，客户端通过将该记号传回服务器要求服务器验证其（客户端）缓存
  2. 304是HTTP状态码，服务器用来标识这个文件没修改，不返回内容，浏览器在接收到个状态码后，会使用浏览器已缓存的文件
  3. 客户端请求一个页面（A）。 服务器返回页面A，并在给A加上一个ETag。 客户端展现该页面，并将页面连同ETag一起缓存。 客户再次请求页面A，并将上次请求时服务器返回的ETag一起传递给服务器。 服务器检查该ETag，并判断出该页面自上次客户端请求之后还未被修改，直接返回响应304（未修改——Not Modified）和一个空的响应体
---

# 说一下和304相关的几个header属性，Etag和last modified有什么区别
  * ETag/If-None-Match
  * Last-Modified/If-Modified-Since
  * 区别：
    1. last-modified 的精确度是秒，相比来说，etag 更加精确。
    2. last-modified 是每次文件修改都会对应修改，即使文件内容并没有改变，相比来说，etag 可以避免部分文件内容未修改的缓存更新。
---

# 什么时候用304？
  如果客户端发送了一个带条件的GET 请求且该请求已被允许，而文档的内容（自上次访问以来或者根据请求的条件）并没有改变，则服务器应当返回这个304状态码。
---

# 301 302 304各自代表了什么，304的协商缓存怎么定义，说一下强缓存
  * 301：Moved Permanently 被请求的资源已永久移动到新位置，并且将来任何对此资源的引用都应该使用本响应返回的若干个URI之一。如果可能，拥有链接编辑功能的客户端应当自动把请求的地址修改为从服务器反馈回来的地址。除非额外指定，否则这个响应也是可缓存的。
  * 302：Found 请求的资源现在临时从不同的URI响应请求。由于这样的重定向是临时的，客户端应当继续向原有地址发送以后的请求。只有在Cache-Control或Expires中进行了指定的情况下，这个响应才是可缓存的。
  * 304：如果客户端发送了一个带条件的GET 请求且该请求已被允许，而文档的内容（自上次访问以来或者根据请求的条件）并没有改变，则服务器应当返回这个304状态码。
---

# 问在HTTP响应Header中，Set-Cookie的选项有哪些？分别是什么含义？
  * name=value: 表示要设置的Cookie的名称和值。
  * expires=date: 指定Cookie的过期时间，如果不设置，Cookie默认在浏览器关闭时过期。
  * domain=domain: 指定Cookie的有效域，控制哪些域可以访问该Cookie。
  * path=path: 指定Cookie的有效路径，控制哪些路径下的页面可以访问该Cookie。
  * secure: 如果设置了该选项，Cookie只能通过HTTPS协议传输。
  * httponly: 如果设置了该选项，Cookie将无法通过JavaScript脚本访问，有助于防止跨站脚本攻击（XSS）。
  * samesite=strict/lax/none: 该选项用于控制跨站请求伪造（CSRF）攻击。strict表示仅在同站点请求时发送Cookie，lax表示在导航到其他站点时不发送Cookie，仅在顶级导航时发送；none表示总是发送Cookie。
---

# If-Modified-Since、If-Match是根据什么进行判断
etag
---

# 什么是Etag？
  > 浏览器下载组件的时候，会将它们存储到浏览器缓存中。如果需要再次获取相同的组件，浏览器将检查组件的缓存时间，假如已经过期，那么浏览器将发送一个条件GET请求到服务器，服务器判断缓存还有效，则发送一个304响应，告诉浏览器可以重用缓存组件。那么服务器是根据什么判断缓存是否还有效呢?答案有两种方式，一种是前面提到的ETag，另一种是根据Last-Modified
---

# 怎么生成ETAG
---

# 协商缓存中etag lastmodify区别
---

# 生成ETAG的算法了解过吗(原理)
---

# 缓存原理，ETAG给服务器的压力太大怎么办
---

# expires的单位是
---

# HTTP和HTTPS的区别。https怎么实现它的安全性的？
  * HTTP协议通常承载于TCP协议之上，在HTTP和TCP之间添加一个安全协议层（SSL或TSL），这个时候，就成了我们常说的HTTPS。默认HTTP的端口号为80，HTTPS的端口号为443。
---

# HTTP2.0和HTTP1.0有什么区别呢
---

# https怎么加密的？(加密流程)，如何通过公钥和私钥加密？
---

# https加密解密过程涉及的算法，这些算法的区别
---

# HTTPS认证是怎么认证的？(SSL证书浏览器是怎么验证的？)
  * 客户端和服务端进行数据传输之前，先通过证书对双方进行身份验证：
    1. 客户端在发送SSL握手信息给服务端要求连接
    2. 服务端会将证书发送给客户端
    3. 客户端检查服务端证书，确认这个这个证书的签发机构是否值得信任，如果检查有问题，客户端会将是否继续通讯的决定权交给客户端，如果检查无误，或者用户选择继续，就表现客户端认可服务端身份。
    4. 服务端要求客户端发送证书，并且检查是否通过验证， 失败就关闭连接，成功的话就得到客户端的公钥
---

# 常见Http请求头
  * Host (主机和端口号)
  * Connection (链接类型)
  * Upgrade-Insecure-Requests (升级为 HTTPS 请求)
  * User-Agent (浏览器名称)
  * Accept (传输文件类型)
  * Referer (页面跳转处)
  * Accept-Encoding（文件编解码格式）
  * Cookie （Cookie）
  * x-requested-with :XMLHttpRequest (是 Ajax 异步请求)
---

# HTTPS原理及过程
  * 客户端在使用HTTPS方式与Web服务器通信时有以下几个步骤，如图所示。
    - 客户使用https url访问服务器，则要求web 服务器建立ssl链接。
    - web服务器接收到客户端的请求之后，会将网站的证书（证书中包含了公钥），返回或者说传输给客户端。
    - 客户端和web服务器端开始协商SSL链接的安全等级，也就是加密等级。
    - 客户端浏览器通过双方协商一致的安全等级，建立会话密钥，然后通过网站的公钥来加密会话密钥，并传送给网站。
    - web服务器通过自己的私钥解密出会话密钥。
    - web服务器通过会话密钥加密与客户端之间的通信。
---

# HTTP协议有什么特点？
  1. 简单快速：客户向服务器请求服务时，只    需传送请求方法和路径。请求方法常用的有GET、HEAD、POST等。每种方法规定了客户与服务器联系的类型不同。由于HTTP协议简单，使得HTTP服务器的程序规模小，因而通信速度很快。

  2. 灵活：HTTP允许传输任意类型的数据对象。正在传输的类型由Content-Type加以标记。

  3. HTTP 0.9和1.0使用非持续连接：限制每次连接只处理一个请求。服务器处理完客户的请求，并收到客户的应答后，即断开连接。HTTP 1.1使用持续连接：不必为每个web对象创建一个新的连接，一个连接可以传送多个对象，采用这种方式可以节省传输时间。

  4. 无状态：HTTP协议是无状态协议。无状态是指协议对于事务处理没有记忆能力。缺少状态意味着如果后续处理需要前面的信息，则它必须重传，这样可能导致每次连接传送的数据量增大。另一方面，在服务器不需要先前信息时它的应答就较快。

  5. 支持B/S(Browser/Server,浏览器/服务器方式的网络结构。)及C/S(Client/Server,客户/服务器方式的网络计算模式)模式。
---

# WebSocket和HTTP之间的关系
  1. WebSocket和HTTP一样都是基于TCP的应用层协议。

  2. WebSocket协议和HTTP协议是两种不同的东西。客户端开始建立WebSocket连接时要发送一个header标记了 Upgrade的HTTP请求，表示请求协议升级。所以服务器端做出响应的简便方法是，直接在现有的HTTP服务器软件和现有的端口上实现WebSocket协议，然后再回一个状态码为101的HTTP响应完成握手，再往后发送数据时就没 HTTP的事了。也就是说WebSocket只是使用HTTP协议来完成一部分握手。
  
  3. http无状态、被动；ws一次握手，知道状态，可以双向通信
---

# websocket，用法，如何保证仍然连接，如何确保消息发送到了，从计网的角度来讲一讲如何保证websocket传输可靠(websocket怎么传送数据的)
---

# websocket是什么，原理，怎么实现
---

# websocket 为什么要加心跳? websocket 不是长连接吗，为什么还要加心跳去维持连接
---

# 心跳监听机制
---

# websocket 连接成功的状态码是多少
---

# WebSocket了解吗？用的什么协议
TCP
---

# 说说http 与 tcp 的关系
---

# tcp 可以建立多个连接吗？
---

# 介绍TCP队头阻塞的问题以及如何解决的？
---

# tcp 握手 回收过程，了解泛洪攻击么；
---

# tcp的拥塞控制和流量控制
---

# tcp如何保证安全连接
---

# TCP/IP有几层网络模型，都是做什么的
---

# TCP跟UDP的区别
---

# TCP是怎么判断丢包的？
---

# 什么情况用TCP,什么情况用UDP?为什么视频使用UDP协议?有什么负面影响?
---

# 说说TCP传输的三次握手四次挥手策略
  * 三次握手:
    1. 为了准确无误地把数据送达目标处，TCP协议采用了三次握手策略。用TCP协议把数据包送出去后，TCP不会对传送 后的情况置之不理，它一定会向对方确认是否成功送达。握手过程中使用了TCP的标志：SYN和ACK。

    2. 发送端首先发送一个带SYN标志的数据包给对方。接收端收到后，回传一个带有SYN/ACK标志的数据包以示传达确认信息。

    3. 最后，发送端再回传一个带ACK标志的数据包，代表“握手”结束。 若在握手过程中某个阶段莫名中断，TCP协议会再次以相同的顺序发送相同的数据包。

  * 断开一个TCP连接则需要“四次挥手”：
    1. 第一次挥手：主动关闭方发送一个FIN，用来关闭主动方到被动关闭方的数据传送，也就是主动关闭方告诉被动关闭方：我已经不 会再给你发数据了(当然，在fin包之前发送出去的数据，如果没有收到对应的ack确认报文，主动关闭方依然会重发这些数据)，但是，此时主动关闭方还可 以接受数据。

    2. 第二次挥手：被动关闭方收到FIN包后，发送一个ACK给对方，确认序号为收到序号+1（与SYN相同，一个FIN占用一个序号）。

    3. 第三次挥手：被动关闭方发送一个FIN，用来关闭被动关闭方到主动关闭方的数据传送，也就是告诉主动关闭方，我的数据也发送完了，不会再给你发数据了。

    4. 第四次挥手：主动关闭方收到FIN后，发送一个ACK给被动关闭方，确认序号为收到序号+1，至此，完成四次挥手。
---

# 为什么是三次握手而不是两次握手
  > 防止已失效的连接请求又传送到服务器端，因而产生错误。这是因为服务端的LISTEN状态下的SOCKET当收到SYN报文的连接请求后，它可以把ACK和SYN（ACK起应答作用，SYN起同步作用）房子啊一个报文里来发送，但关闭连接时，当收到对方的FIN报文通知时，它仅仅表示对方没有数据发送给你了，但未必你所有的数据都发送给对方了，所以你可能未必会马上关闭SOCKET，即你可能还需要发送一个数据给对方之后，再发送DIN报文给对方来表示你同意现在可以关闭连接了，所以他这里的ACK报文和FIN报文多数情况下都是分开发送的
---

# HTTP和HTTPS的区别。https怎么实现它的安全性的？
  * HTTP协议通常承载于TCP协议之上，在HTTP和TCP之间添加一个安全协议层（SSL或TSL），这个时候，就成了我们常说的HTTPS。默认HTTP的端口号为80，HTTPS的端口号为443。
---

# 怎么理解端到端的连接？
---

# HTTP的协议格式
---

# 怎么判断HTTP报文传输完成了
---

# 对称加密和非对称加密的了解
  ![面试题](/images/vue/面试题.jpg)
---

# SSL协议是使用对称加密还是非对称加密
对称加密和非对称加密相结合
---

# 非对称加密耗时久，怎么优化?
---

# http工作原理
  1. 客户端连接到Web服务器 
  2. 发送HTTP请求
  3. 服务器接受请求并返回HTTP响应
  4. 释放连接TCP连接
  5. 客户端浏览器解析HTML内容
---

# HTTPS原理及过程
---

# HTTP/2能节省连接时间吗?
---

# HTTP/2会有队头阻塞问题吗?
---

# 三次握手的过程 客户端和服务端都做了什么？
---

# http是无连接的？
---

# http属于哪一层，tcp和ip呢
---

# Tcp如何保证可靠传输
---

# Udp如何实现可靠传输
---

# 域名解析属于udp还是tcp？
udp
---

# quic 协议原理
---

# HTTP2.0的多路复用和HTTP1.1的长连接有什么区别
  * 1.x默认开启持久连接，在一个TCP连接上可以传送多个http请求和相应，减少了简历和关闭连接的小号和延迟
  * 多路复用是长链接的升级版。多路复用，就是在一个TCP连接中可以发送多个请求，服务端可以通过帧中的标识知道该帧属于哪个请求，通过重新排序还原请求。多路复用允许并发的发起多个请求，每个请求及该请求的响应不需要等待其他的请求或响应，避免了线头阻塞问题。这样某个请求任务耗时严重，不会影响到其他链接的正常执行，极大的提高传输性能
---

# http2和http3的区别
---

# 对 http 几个版本有什么区别？keep-alive 和 多路复用在性能上有什么区别？为什么 keep-alive 可以达到多路复用的效果？
---

# 你知道哪些常见的header中的字段
---

# 说一下浏览器缓存；
  1. 浏览器缓存分为强缓存和协商缓存，强缓存会直接从浏览器里面拿数据，协商缓存会先访问服务器看缓存是否过期，再决定是否从浏览器里面拿数据。
  2. 控制强缓存的字段有：Expires和Cache-Control，Expires 和 Cache-Control。
  3. 控制协商缓存的字段是：Last-Modified / If-Modified-Since 和 Etag / If-None-Match，其中 Etag / If-None-Match的优先级比Last-Modified / If-Modified-Since高。
---

# 强缓存和协商缓存
---

# 强缓存一般放在哪里？
  一般放在Memory cache或者disk cache;
---

# 计算整个文件得到etag会耗费心力，怎么解决？
  > etag可以通过文件的lastModified和content-length计算
---

# 如果我不想要使用缓存了，每次都请求最新的，怎么做？
  通过url拼接rendom的方式或者设置cache-control设置为no-cache
---

# cache-control中的no-cache和no-store的差异
  * no-store禁止浏览器和中间服务器缓存，每次都从服务器获取
  * no-cache每次请求都会验证该缓存是否过期，可以存在本地缓存，可以在代理服务器缓存，但是这个缓存要服务器验证才可以使用
---

# 请介绍下cache-control
  * cache-control是一个通用消息头字段被用于HTTP请求和响应中，通过指定指令来实现缓存机制，这个缓存指令是单向的，常见的取值有private、no-cache、max-age、must-revalidate等，默认为private。
  * 每个资源都可以通过 Cache-Control HTTP 头来定义自己的缓存策略
  * Cache-Control 指令控制谁在什么条件下可以缓存响应以及可以缓存多久
  * Cache-Control 头在 HTTP/1.1 规范中定义，取代了之前用来定义响应缓存策略的头（例如 Expires）。
---

# 浏览器缓存机制有哪几种；HTTP缓存有几种，原理是什么？
  * 浏览器缓存机制：
    1. http缓存
    2. websql
    3. indexDB
    4. Cookie
    5. Localstorage、Sessionstorage
    6. application cache
    7. cacheStorage
    8. flash缓存
  * HTTP缓存种类：
    1. 强缓存
    2. 协商缓存
  * 介绍：
    - 缓存就是让同一份资源不再发起请求，降低网络压力和资源数量，从而让网页加载更快。 网络请求不稳定加剧了网页加载的不稳定性，所以需要缓存。 一般来说，js、css、img等静态资源可以被缓存
  * 原理：
    - 强缓存：服务器通知浏览器一个缓存时间，在缓存时间内，下次请求，直接用缓存，不在时间内，执行比较缓存策略。
    - 协商缓存：将缓存信息中的Etag和Last-Modified通过请求发送给服务器，由服务器校验，返回304状态码时，浏览器直接使用缓存。
---

# 有了 Last-Modified 为什么还要有 Etag
---

# 为什么有了 Expires 还要有 Cache-Control？Expires  会造成什么问题
---

# http的缓存，强缓存和弱缓存有什么区别？他们的一些请求头和响应头是怎么样的？强缓存命中的时候，请求回返回什么样的状态码？
---

# 如果现在对资源启用强缓存，那如何判断资源是否更新呢（说webpack hash），hash是如何生成的呢
---

# 线程与进程的区别
  * 一个程序至少有一个进程,一个进程至少有一个线程. 
  * 线程的划分尺度小于进程，使得多线程程序的并发性高。
  * 另外，进程在执行过程中拥有独立的内存单元，而多个线程共享内存，从而极大地提高了程序的运行效率。 
  * 线程在执行过程中与进程还是有区别的。每个独立的线程有一个程序运行的入口、顺序执行序列和程序的出口。但是线程不能够独立执行，必须依存在应用程序中，由应用程序提供多个线程执行控制。 
  * 从逻辑角度来看，多线程的意义在于一个应用程序中，有多个执行部分可以同时执行。但操作系统并没有将多个线程看做多个独立的应用，来实现进程的调度和管理以及资源分配。这就是进程和线程的重要区别。
---

# 线程共享为什么比进程共享容易？

---

# 进程调度
---

# 进程之间和线程之间如何通信
---

# 前端安全问题？
  1. iframe
    * 如何让自己的网站不被其他网站的 iframe 引用？
      - 通过判断`top.location`是否等于`self.location`，不等让他调转到百度
    * 如何禁用，被使用的 iframe 对当前网站某些操作？
      - 可以通过设置sandbox属性。sandbox是html5的新属性，主要是提高iframe安全系数。

  2. CSRF（跨站请求伪造）
    * 你可以这么理解 CSRF 攻击：攻击者盗用了你的身份，以你的名义进行恶意请求。它能做的事情有很多包括：以你的名义发送邮件、发信息、盗取账号、购买商品、虚拟货币转账等。
    * 阐述 CSRF 攻击思想：
      1、浏览并登录信任网站（举例：淘宝）
      2、登录成功后在浏览器产生信息存储（举例：cookie）
      3、用户在没有登出淘宝的情况下，访问危险网站
      4、危险网站中存在恶意代码，代码为发送一个恶意请求（举例：购买商品/余额转账）
      5、携带刚刚在浏览器产生的信息进行恶意请求
      6、淘宝验证请求为合法请求（区分不出是否是该用户发送）
      7、达到了恶意目标
    * 防御措施：
      - 涉及到数据修改操作严格使用 post 请求而不是 get 请求
      - HTTP 协议中使用 Referer 属性来确定请求来源进行过滤（禁止外域）
      - 请求地址添加 token ，使黑客无法伪造用户请求
      - HTTP 头自定义属性验证（类似上一条）
      - 显示验证方式：添加验证码、密码等

  3. XSS（跨站脚本攻击）
    * 跨站脚本攻击：攻击者在目标网站植入恶意脚本（js / html），用户在浏览器上运行时可以获取用户敏感信息（cookie / session）、修改web页面以欺骗用户、与其他漏洞相结合形成蠕虫等。
    * XSS类型：
      - 持久型XSS：将脚本植入到服务器上，从而导致每个访问的用户都会执行
      - 非持久型XSS：对个体用户某url的参数进行攻击
    * 针对这种情况，我们对特殊字符进行转译就好了（vue/react等主流框架已经避免类似问题，vue举例：不能在template中写script标签，无法在js中通过ref或append等方式动态改变或添加script标签）

  4. ClickJacking（点击劫持）
    * 一般会利用透明 iframe 覆盖原网页诱导用户进行某些操作达成目的。
    * 防御措施：
      - 在HTTP投中加入 X-FRAME-OPTIONS 属性，此属性控制页面是否可被嵌入 iframe 中【DENY：不能被所有网站嵌套或加载；SAMEORIGIN：只能被同域网站嵌套或加载；ALLOW-FROM URL：可以被指定网站嵌套或加载。】 判断当前网页是否被 iframe 嵌套（详情在第一条 firame 中）
---

# sql注入原理
---

# 什么是运营商劫持？
  > 网页登录运营商会给你的网页页面上加上各种页面里本来没有的广告。劫持方式分为DNS劫持、HTTP劫持、HTTPS劫持3种
---

# 运营商劫持怎么处理
  * 主要是防script、iframe注入
---

# 请解释一下csrf 和 xss；
  * xss：XSS全称cross-site scripting（跨站点脚本），是一种代码注入攻击，是当前 web 应用中最危险和最普遍的漏洞之一。攻击者向网页中注入恶意脚本，当用户浏览网页时，脚本就会执行，进而影响用户**，比如关不完的网站、盗取用户的 cookie 信息从而伪装成用户去操作，危害数据安全。

  * csrf：CSRF 跨站请求伪造（英语：Cross-site request forgery），是一种挟制用户在当前已登录的 Web 应用程序上执行非本意的操作的攻击方法。如： 攻击者诱导受害者进入第三方网站，在第三方网站中，向被攻击网站发送跨站请求。利用受害者在被攻击网站已经获取的注册凭证，绕过后台的用户验证，达到冒充用户对被攻击的网站执行某项操作的目的。
---

# 怎么防止 csrf 和 xss？
  * XSS:
    1. 将重要的cookie标记为http only, ，浏览器将禁止页面的 JavaScript 访问带有 HttpOly 属性的 Cookie。
    2. HttpOnly 主要是为了解决 XSS 之后的 Cookie 劫持，使用 HttpOnly 有助于缓解 XSS 攻击，防止被窃取敏感的 Cookie信息，本质上不是 为了解决 XSS。
    3. 在输入输出时对数据进行转义，比如<转义成<,这样脚本就运行不了了
    4. 录入数据设置白名单，比如javaWeb项目，设置过滤器过滤特殊字符
    5. 前端页面限制用户输入数据类型，比如用户输入完年龄后验证输入内容只能是数字
    6. 过滤JS事件的标签，比如onclick、load等

  * csrf:
    1. token；token 验证的 CSRF 防御机制是公认最合适的方案。但若网站同时存在 XSS 漏洞的时候，这个方法也是空谈
    2. 验证码；强制用户必须与应用进行交互，才能完成最终请求。此种方式能很好的遏制 csrf，但是用户体验比较差
    3. Referer check；请求来源限制，此种方法成本最低，但是并不能保证 100% 有效，因为服务器并不是什么时候都能取到 Referer，而且低版本的浏览器存在伪造 Referer 的风险
---

# 怎么解决refer伪造？
---

# XSS是什么，攻击原理，怎么预防。
---

# XSS攻击的场景能描述一个么？
---

# 请说说XSS与CSRF
  * ![xss](/images/math/xss与csrf.png)
  * ![xss](/images/math/xss与csrf2.png)
  * ![xss](/images/math/xss与csrf3.png)
  * ![xss](/images/math/xss与csrf4.png)
  * ![xss](/images/math/xss与csrf5.png)
---

# 服务端劫持了 token 怎么做防御
---

# 服务端反爬虫
---

# 服务端跨域应该如何设置
---

# GET和POST的区别，何时使用POST？
  * 区别:
    1. GET：一般用于信息获取，使用URL传递参数，对所发送信息的数量也有限制，一般在2000个字符
    2. POST：一般用于修改服务器上的资源，对所发送的信息没有限制。
    3. GET方式需要使用Request.QueryString来取得变量的值，而POST方式通过Request.Form来获取变量的值，也就是说Get是通过地址栏来传值，而Post是通过提交表单来传值。

  * 然而，在以下情况中，请使用 POST 请求：
    1. 无法使用缓存文件（更新服务器上的文件或数据库）
    2. 向服务器发送大量数据（POST 没有数据量限制）
---

# 描述以下POST和PUT的区别
---

# 介绍下options请求
---

# options预检请求了解吗，返回什么
---

# contentType 有哪些，有什么作用
---

# 简单请求和复杂请求的区别
---

# x-www-urlecoded-form和application/json在post中的区别
  * application/x-www-form-urlencoded：我bai们form表单提交就是这个模式，du并且将zhi提交的数据进行daourlencode。默认情况下，我zhuan们所有的表单提交都是通过这种默shu认的方式实现的。最常用的一种。

  * application/json：采用json格式提交，比如我们常用的ajax，dataType:"json"
---

# REST是什么, 为什么使用它?
---

# 遇到过哪些移动端兼容问题？
---

# 如何优化SPA应用的首屏加载速度慢的问题？
  1. 使用webpack打包，压缩代码，实现按需加载
  2. 使用缓存
  3. script 设置defer/async
  4. 使用图片懒加载，对滚动事件实现防抖节流操作，防止不停触发事件
  5. 减少重排重绘
  6. 使用预加载preload/prefetch
---

# SPA理解和原理
---

# 对于首屏就必须要加载的包，有什么优化手段
使用http缓存必须使用的包，下次请求时从缓存读取
---

# 怎么知道一个tcp请求数据已经完了呢
---

# 项目里面的鉴权和图片懒加载怎么实现的
---

# 路由鉴权如何实现，如果是不同身份怎么重定向到未认证页面，死扣细节，代码实现
---

# 如何更好的处理线上的日志？
  1. 日志分级输出，可以分业务日志错误日志等
  2. 可以把日志交给spring管理，定期扫描配置文件达到无需重启的目的，定位到原因就可以把级别调回去
  3. 把日志放到WEB目录，通过权限限制外网直接访问，达到浏览器就可以查看日志
---

# 组件设计原则。
  1. 层次结构和 UML 类图；
  2. 扁平化、面向数据的 state/props；
  3. 更加纯粹的 State 变化；
  4. 低耦合；
  5. 辅助代码分离；
  6. 及时模块化；
  7. 集中/统一的状态管理；
---

# 介绍下web worker，有什么用，什么样的场景比较适合？
---

# 发布订阅模式和观察者模式的异同。
---

# TCP/IP有几层网络模型，都是做什么的(网络层次结构)
---

# 数据链路层解决什么问题
---

# TCP怎么保证有序
他必须收到上一个数据帧的ACK后才发下一个数据
---

# 数组和链表的区别，什么时候用链表，什么时候用数组
  1. 存储位置上：数组逻辑上相邻的元素在物理存储位置上也相邻，而链表不一定；
  2. 存储空间上：链表存放的内存空间可以是连续的，也可以是不连续的，数组则是连续的一段内存空间。一般情况下存放相同多的数据数组占用较小的内存，而链表还需要存放其前驱和后继的空间。
  3. 长度的可变性：链表的长度是按实际需要可以伸缩的，而数组的长度是在定义时要给定的，如果存放的数据个数超过了数组的初始大小，则会出现溢出现象。
  4. 按序号查找时，数组可以随机访问，时间复杂度为O(1)，而链表不支持随机访问，平均需要O(n)；　
  5. 按值查找时，若数组无序，数组和链表时间复杂度均为O(1)，但是当数组有序时，可以采用折半查找将时间复杂度降为O(logn)；　
  6. 插入和删除时，数组平均需要移动n/2个元素，而链表只需修改指针即可；　
  7. 空间分配方面：数组在静态存储分配情形下，存储元素数量受限制，动态存储分配情形下，虽然存储空间可以扩充，但需要移动大量元素，导致操作效率降低，而且如果内存中没有更大块连续存储空间将导致分配失败； 即数组从栈中分配空间,，对于程序员方便快速,但自由度小。链表存储的节点空间只在需要的时候申请分配，只要内存中有空间就可以分配，操作比较灵活高效；即链表从堆中分配空间, 自由度大但申请管理比较麻烦。
---

# 链表和数组进行插入和删除的时间复杂度
---

# 链表的类型以及应用场景
---

# 树的类型以及应用场景，说一下红黑树和B+树
---

# 项目自动部署流程
---

# 网站如何反爬虫
---

# 网页上实现VR效果的原理
---

# 网页上实现VR效果的原理
---

# 实现IM聊天流程，以及做过哪些优化
---

# 实现一个i18n国际化的思路，部分动态替换的数据如何处理
---

# 小组工作流程
  1. 拿到原型图，先自我解析需求
    * 依赖的外部资源
      - 后端提供的接口
      - ui出图的大概布局
      - 后期频繁改动的地方
    * 需要事先的效果
      - 下拉刷新
      - 动画效果
      - 吸顶效果
      - 懒加载、预加载、防抖、节流
  2. 产品召集项目相关人员，开需求讨论会，产品讲解原型
    * 理解产品的需求，提出疑问：这是什么功能、怎么做、为啥这么做
    * 评估实现难度和实现成本，是否有潜在技术问题/风险
    * 对比自己理解的需求图，如果有和自己想的不符合的，提出疑问
    * 理解需求方提出此次需求的目的，分清主次，可以适当取舍
    * 如果要求提供上线时间，简单项目可以预估，复杂项目要仔细评估，不可马上给出时间
  3. 进一步整理需求
    * 细化细节，整理有疑问的地方，找对应的人员进行确认
    * 评估完成时间
    * 初步制定排期表
  4. 开发
    * 技术选型
    * 搭建开发环境：工具链
    * 搭建项目架构
    * 业务模块划分
      - 优先级排序
      - 新项目介入，需要当前项目和介入项目的相关负责人pk优先级，随后调整项目排期
      - 开发过程中发现工作量与预期有严重出入，需要尽早向其他项目人员反馈，方便其修改时间安排
  5. 顶置开发规范
    * 开发规范
      - commit提交格式：[改动文件类型]：[改动说明]
      - 单分支开发或者多分支开发
        1. 小项目、并行开发少，则只在master主分支开发
        2. 中大项目，需求复杂，并行功能多，则需要建多个分支,master,dev，开发者分支；需要开发者自创一个分支开发，合并到dev，确认无问题后发布到master，最后上线
    * 代码规范
    * 源码管理
    * 版本管理
    * 安全管理
  6. 自测
    * 手动测试
    * 单元测试
    * 集成测试
  7. 提测-测试人员测试
    * 开发人员修复bug
    * 期间不可接受耗时大的需求
    * 又不确定优先级高低的需求，需要讨论，取舍
    * 测试修复bug时间可能比开发时间还长，因此开发者预估开发时间不能乐观
  8. 上线
    * 上线准备：域名申请、备案申请、服务器申请、部署
    * 测试线上环境：有bug回到修复bug环节
    * 日志监控
  9. 维护
---

# 登陆保持方法
---

# 项目中最难的部分
---

# 单页和多页应用差别及优缺点
  * 单页面应用（SPA），通俗一点说就是指只有一个主页面的应用，浏览器一开始要加载所有必须的 html, js, css。所有的页面内容都包含在这个所谓的主页面中。但在写的时候，还是会分开写（页面片段），然后在交互的时候由路由程序动态载入，单页面的页面跳转，仅刷新局部资源。多应用于pc端。
  * 多页面（MPA），就是指一个应用中有多个页面，页面跳转时是整页刷新
  * 单页面的优点：
    1. 用户体验好，快，内容的改变不需要重新加载整个页面，基于这一点spa对服务器压力较小
    2. 前后端分离
    3. 页面效果会比较炫酷（比如切换页面内容时的专场动画）
  * 单页面缺点：
    1. 不利于seo
    2. 导航不可用，如果一定要导航需要自行实现前进、后退。（由于是单页面不能用浏览器的前进后退功能，所以需要自己建立堆栈管理）
    3. 初次加载时耗时多
    4. 页面复杂度提高很多
---

# 对链表进行循环，判断是不是一个环
---

# 怎么实现一个eventBus
---

# 二分法时间复杂度
---

# 在https页面能不能发http请求
---

# 允许在https页面插http资源吗
---

# 有了解 http 轮询吗
---

# 传统轮询有没有可能发两次请求后发的请求先返回数据？怎么解决（如何保证响应顺序）
---

# 你们的代码存在哪里啊，通过什么管理的
---

# 文件断点上传，怎么实现；
  * 前端：
    - 前端大文件上传网上的大部分文章已经给出了解决方案，核心是利用 Blob.prototype.slice 方法，和数组的 slice 方法相似，调用的 slice 方法可以返回原文件的某个切片
    - 这样我们就可以根据预先设置好的切片最大数量将文件切分为一个个切片，然后借助 http 的可并发性，同时上传多个切片，这样从原本传一个大文件，变成了同时传多个小的文件切片，可以大大减少上传时间
    - 另外由于是并发，传输到服务端的顺序可能会发生变化，所以我们还需要给每个切片记录顺序
  * 服务端：
    - 服务端需要负责接受这些切片，并在接收到所有切片后合并切片
  * 这里又引伸出两个问题。何时合并切片，即切片什么时候传输完成 如何合并切片？
    - 第一个问题需要前端进行配合，前端在每个切片中都携带切片最大数量的信息，当服务端接受到这个数量的切片时自动合并，也可以额外发一个请求主动通知服务端进行切片的合并
    - 第二个问题，具体如何合并切片呢？这里可以使用 nodejs 的 api fs.appendFileSync，它可以同步地将数据追加到指定文件，也就是说，当服务端接受到所有切片后，先创建一个最终的文件，然后将所有切片逐步合并到这个文件中
---

# git和svn的区别？
  1. 最核心的区别Git是分布式的，而Svn不是分布的。
  2. Git把内容按元数据方式存储，而SVN是按文件
  3. Git没有一个全局版本号，而SVN有
  4. Git下载下来后，在OffLine状态下可以看到所有的Log,SVN不可以。
---

# 介绍一下git的开发流程
  1. 克隆 Git 资源作为工作目录。
  2. 在克隆的资源上添加或修改文件。
  3. 如果其他人修改了，你可以更新资源。
  4. 在提交前查看修改。
  5. 提交修改。
  6. 在修改完成后，如果发现错误，可以撤回提交并再次修改并提交。
---

# Git如果commit了内容想要回退该怎么做
---

# git reset 与 revert 区别，revert 多个 mr 改如何处理；
---

# git 如何撤回 add 后的内容；
---

# 什么是“git cherry-pick”?
  * 命令 git cherry-pick 通常用于把特定提交从存储仓库的一个分支引入到其他分支中。常见的用途是从维护的分支到开发分支进行向前或回滚提交。命令git cherry-pick可以把branch A的commit复制到branch B上
---

# git fetch和 git pull的区别
  * 简单来说：git fetch branch是把名为branch的远程分支拉取到本地；而git pull branch是在fetch的基础上，把branch分支与当前分支进行merge；因此pull = fetch + merge。
---

# git rebase和git merge的区别
  * 简单的说，git merge和git rebase都是合并分支的命令。
  * git merge branch会把branch分支的差异内容pull到本地，然后与本地分支的内容一并形成一个committer对象提交到主分支上，合并后的分支与主分支一致；
  * git rebase branch会把branch分支优先合并到主分支，然后把本地分支的commit放到主分支后面，合并后的分支就好像从合并后主分支又拉了一个分支一样，本地分支本身不会保留提交历史。
---

# 谈谈git flow
  * GitFlow可以用来管理分支。GitFlow工作流中常用的分支有下面几类：
    - master分支：最为稳定功能比较完整的随时可发布的代码，即代码开发完成，经过测试，没有明显的bug，才能合并到 master 中。请注意永远不要在 master 分支上直接开发和提交代码，以确保 master 上的代码一直可用；
    - develop分支；用作平时开发的主分支，并一直存在，永远是功能最新最全的分支，包含所有要发布 到下一个 release 的代码，主要用于合并其他分支，比如 feature 分支； 如果修改代码，新建 feature 分支修改完再合并到 develop 分支。所有的 feature、 release 分支都是从 develop 分支上拉的。
    - feature分支；这个分支主要是用来开发新的功能，一旦开发完成，通过测试没问题（这个测试，测试新功能没问题），我们合并回develop 分支进入下一个 release
    - release分支；用于发布准备的专门分支。当开发进行到一定程度，或者说快到了既定的发布日，可以发布时，建立一个 release 分支并指定版本号(可以在 finish 的时候添加)。开发人员可以对 release 分支上的代码进行集中测试和修改bug。（这个测试，测试新功能与已有的功能是否有冲突，兼容性）全部完成经过测试没有问题后，将 release分支上的代码合并到 master 分支和 develop 分支
    - hotfix分支；用于修复线上代码的bug。从 master 分支上拉。完成 hotfix 后，打上tag 我们合并回 master 和 develop 分支。
  * GitFlow主要工作流程
    1. 初始化项目为gitflow , 默认创建master分支 , 然后从master拉取第一个develop分支
    2. 从develop拉取feature分支进行编码开发(多个开发人员拉取多个feature同时进行并行开发 , 互不影响) 
    3. feature分支完成后 , 合并到develop(不推送 , feature功能完成还未提测 , 推送后会影响其他功能分支的开发)；合并feature到develop , 可以选择删除当前feature , 也可以不删除。但当前feature就不可更改了，必须从release分支继续编码修改
    4. 从develop拉取release分支进行提测 , 提测过程中在release分支上修改BUG 
    5. release分支上线后 , 合并release分支到develop/master并推送；合并之后，可选删除当前release分支，若不删除，则当前release不可修改。线上有问题也必须从master拉取hotfix分支进行修改；
    6. 上线之后若发现线上BUG , 从master拉取hotfix进行BUG修改；
    7. hotfix通过测试上线后，合并hotfix分支到develop/master并推送；合并之后，可选删除当前hotfix ，若不删除，则当前hotfix不可修改，若补丁未修复，需要从master拉取新的hotfix继续修改；
    8. 当进行一个feature时 , 若develop分支有变动 , 如其他开发人员完成功能并上线 , 则需要将完成的功能合并到自己分支上，即合并develop到当前feature分支；
    9. 当进行一个release分支时 , 若develop分支有变动 , 如其他开发人员完成功能并上线 , 则需要将完成的功能合并到自己分支上，即合并develop到当前release分支 (!!! 因为当前release分支通过测试后会发布到线上 , 如果不合并最新的develop分支 , 就会发生丢代码的情况)； GitFlow的好处为不同的分支分配一个明确的角色，并定义分支之间如何交互以及什么时间交互；可以帮助大型项目理清分支之间的关系，简化分支的复杂度。
---

# Git的快照是指什么？Git的工作区域由哪三部分组成？在git中，如何为提交的版本打标签
  * 快照：git会把出现变更的文件直接拷贝，形成新的blob，而非与上一个版本的diff，并记录下来。并非每个当前版本都需要做备份，如果没有改变，那么快照其实是链接上一个版本。
  
  * 三部分：
    - 工作区：用户本地的工作目录
    - 暂存区：一个临时的用于放置文件修改动作的缓存区域
    - 版本库：包含了所有版本及分子的仓库。该仓库里面的文件能够被git说管理，文件的添加、删除、修改都能被git所跟踪
  
  * git的工作流程：
    - 在工作区增删改文件；
    - 将修改后的文件放到暂存区域
    - 将暂存区域的文件提交到本地仓库
    - 将本地仓库的修改推送到远程仓库
  * 如何打标签：
    1. 切换到需要打标签的分支，执行add，commit操作
    2. 输入git tag `<name>`新建标签
    3. 推送到远端仓库
---

# get rebase的作用
  > 会把branch分支优先合并到主分支，然后把本地分支的commit放到主分支后面，合并后的分支就好像从合并后主分支又拉了一个分支一样，本地分支本身不会保留提交历史。
---

# 讲讲二叉树
---

# 讲讲红黑二叉树和平衡二叉树
---

# 前端渲染和服务端渲染在用户体验上有什么差别？
---

# JPG和PNG图片的应用场景，哪一个质量低，两者区别。
---

# 登录功能怎么实现
---

# 前后端交互怎么确定用户身份？
---

# 跨域部署怎么传cookie？
https://blog.csdn.net/weixin_44862325/article/details/105605091
---

# Token的机制是怎样的
---

# token存在哪里
---

# token的产生方法与使用的原因
---

# 每次发起请求都会携带token吗
---

# 怎么做到关掉页面后还能维持登录状态
---

# 登录之后，每次请求一定会携带cookie吗
---

# 发起请求时怎么知道携带哪个cookie，怎么匹配cookie
---

# 有了解过withCredentials属性吗
---

# 互斥登录怎么实现
---

# 单点登录（原理）
  * 概念：
    单点登录SSO，是一个多系统共存的环境下，用户在统一登陆后，就不用在其他系统中登录，也就是用户的一次登录得到其他所有系统的信任
  * 单点登录有同域和跨域两种场景
    - 同域：
      - 试用场景：都是企业自己的系统，所有系统都使用同一个一级域名通过不同的二级域名来区分
      - 核心原理：
        1. 门户系统设置的cookie的domain为一级域名也是zit.com，这样就可以共享门户的cookie给所有的使用该域名zit.com系统
        2. 使用spring session等技术让所有系统共享session
        3. 这样只要门户系统登录之后无论跳转应用1或者应用2，都能通过门户Cookie中的sessionId读取到Session中的登录信息实现单点登录
    - 跨域：
      - 核心原理：
        1. 用户在第一次访问应用系统的时候，因为没有登录，会被引导到认证系统中进行登录；
        2. 根据用户提供的登录信息，认证系统进行身份校验，如果通过，返回给用户一个认证凭据-令牌
        3. 用户再次访问别的应用的时候，带上令牌作为认证凭证
        4. 应用系统接收到请求后会把令牌送到认证服务器进行校验，如果通过，用户可以在不用登陆的情况下访问其他信任的业务服务器
---

# 当请求的文件很大的时候该怎么办
---

# 对于一个盲人用户来讲，如何实现页面元素不可见，但是仍然能够被阅读器识别？
---

# 小程序的文件类型
  * WXML —— 模板文件
  * JSON —— 配置/设置文件，如标题、tabbar、页面注册
  * WXSS —— 样式文件，样式可直接用import导入
  * JS —— 脚本逻辑文件，逻辑处理，网络请求
  * app.json —— 配置文件入口，整个小程序的全局配置，网络超时时间、底部tab、页面路径，window字段是小程序所有页面的顶部背景颜色、文字颜色
  * app.js —— 可以没有内容，可以在里边监听声明周期函数、声明全局变量
  * app.wxss —— 全局配置样式文件
---

# 小程序数据请求怎么封装
  * 将所有的接口放在统一的js文件中并导出（或者将请求地址、头、方法在一个js文件里统一定义为一个常量输出）
  * 在app.js创建封装请求数据的方法
  * 在子页面中调用封装的方法请求数据
---

# 小程序参数传值的方法
  * 给html元素中添加data-*属性来传递需要的值，之后通过e.currentTarget.dataset或onload的param参数获取，注意不能有大小写字母，不可存放对象
  * 跳转页面时通过navigator传递需要的参数值
  * 设置id的方法标识，通过e.currentTarget.id获取设置的id值，然后通过设置全局变量的方法来传递数值
---

# 小程序页面间传值的方式
  * url
  * storag（wx.storageSync）
  * 全局变量（getApp）
---

# 小程序的setData()是怎么实现数据响应式的
---

# 小程序bindtap和catchtap的区别是什么
  * bindtap不会阻止事件冒泡
  * catchtap阻止事件冒泡
---

# 小程序setData的回调函数
  > 微信小程序的setData实现是和react的setState实现类似的，所以它也是一个异步函数，并且有回调函数的参数，当然平时小量数据我们可能并没有感觉到它的异步，但是为了确保逻辑的正确执行，在需要用到setData后，data里的数据的步骤，请写入setData的回调函数中，
---

# 小程序关联微信公众号如何确定用户的唯⼀性
  * 使用wx.getUserInfo ⽅法withCredentials 为true 时可获取encryptedData ， 里面有union_id 。后端需要进行对称解密
---

# 如何看待小程序，它的技术原理是?
  * 微信小程序是一种运行在微信客户端，无需下载和安装。
  * 优点：
    - 无需下载
    - 打开速度快
    - 开发成本低
    - 为用户提供良好的安全保障，发布有一套严格的审查流程，不能通过审查的程序无法发布上线
    - 
  * 缺点：
    - 依托微信，不能开发后台管理功能
    - 大小不能超过2M，不能打开超过5个层级的页面

  * 原理：小程序分为两个部分webview和appService，webview用来展现ui，appService用来处理业务逻辑、数据及接口调用，它们在两个进程中运行，通过系统层JSBridge实现通信，完成ui渲染、事件处理
---

# 小程序上面有做什么性能优化吗？
  * 减少默认data的大小
  * 组件化方案，封装公用组件，减少代码量
---

# 小程序的底层架构是怎么样的？
---

# 小程序生命周期
  * onload —— 页面加载，调一次
  * onShow —— 页面显示，每次打开页面都调用（路由变化就调用）
  * onReady —— 初次渲染完成，调一次
  * onHide —— 页面隐藏，当navigateTo或底部tab切换时调用
  * onUnload —— 页面卸载，当redirectTo或navigateBack时调用
---

# 小程序如何实现下拉刷新？
  * 先在app.json或page.json中配置enablePullDownRefresh:true
  * page里用onPullDownRefresh函数，在下拉刷新时执行
  * 在下拉函数执行时发起数据请求，请求返回后，调用wx.stopPullDownRefresh停止下拉刷新的状态
---

# 小程序的像素rpx计算方式
---

# 小程序双线程模型
---

# 小程序为什么是双线程
  * 小程序之所以有两个线程，是为了实现小程序的高效运行和良好的用户体验。
    1. 渲染线程（UI 线程）： 渲染线程负责小程序界面的渲染和响应用户的交互。它使用 WebView 进行页面渲染，包括解析和绘制 DOM、布局、样式计算和渲染等操作。渲染线程是单线程的，所有的界面操作都在这个线程中进行。
    2. 逻辑线程（JS 线程）： 逻辑线程负责小程序的逻辑运算和数据处理。它是基于 JavaScript 运行的，负责处理用户交互、业务逻辑、数据请求、事件处理等操作。逻辑线程是独立于渲染线程的，可以并行处理多个任务，避免阻塞界面的渲染和响应。
  * 好处：
    1. 响应速度：逻辑线程和渲染线程分开，可以并行执行，提高了小程序的响应速度和用户体验。
    2. 防止阻塞：逻辑线程的运行不会阻塞渲染线程，避免了长时间的计算或数据处理导致界面卡顿或无响应的情况。
    3. 资源隔离：渲染线程和逻辑线程是独立的，它们有各自的资源和运行环境，可以避免相互干扰和影响。
  * 需要注意的是，小程序的渲染线程和逻辑线程之间通过微信客户端进行通信和交互。逻辑线程可以发送请求给微信客户端，然后客户端将渲染指令发送给渲染线程进行界面渲染，同时渲染线程可以将用户的交互事件发送给逻辑线程进行处理。这种通信方式保证了渲染和逻辑的协同工作，实现了小程序的正常运行。
  * 小程序之所以有两个线程，是为了提高渲染速度、避免阻塞和资源隔离。渲染线程负责界面渲染，逻辑线程负责业务逻辑和数据处理，两者通过微信客户端进行通信和交互，共同实现小程序的功能和性能。
---

# 小程序项目的登录如何实现的,用户退出后下次进入还需要再次授权吗
  * wx.login获取到一个code，拿到code去请求后台得到openId, sessionKey, unionId
  * 调用wx.getUserInfo
  * 一次性授权
  * 永久授权：调取授权登录接口并把获取到的用户公开信息存入数据库
---

# 小程序验证授权是自动弹出还是触发的
  > 按钮触发的，open-type指定为getUserInfo类型
---

# 小程序关联公众号如何确定用户的唯一性
  > unionid是相同唯一的
---

# 小程序遇到调试问题
---

# 小程序的原生组件实现原理
---

# 小程序有什么css不能用？
---

# wepy把vue语法转换成原生小程序的原理
---

# 小程序的用户鉴权机制
---

# 小程序与H5的区别？
  1. 运行环境的不同
    * 传统的HTML5的运行环境是浏览器，包括webview，而微信小程序的运行环境并非完整的浏览器，是微信开发团队基于浏览器内核完全重构的一个内置解析器，针对小程序专门做了优化，配合自己定义的开发语言标准，提升了小程序的性能。
  2. 开发成本的不同
    * 只在微信中运行，所以不用再去顾虑浏览器兼容性，不用担心生产环境中出现不可预料的奇妙BUG
  3. 获取系统级权限的不同
    * 系统级权限都可以和微信小程序无缝衔接
  4. 应用在生产环境的运行流畅度
    * 长久以来，当HTML5应用面对复杂的业务逻辑或者丰富的页面交互时，它的体验总是不尽人意，需要不断的对项目优化来提升用户体验。但是由于微信小程序运行环境独立
---

# 小程序的双向绑定和vue哪里不一样？
  小程序直接this.data的属性是不可以同步到视图的，必须调用：this.setData
---

# 简述下 wx.navigateTo(), wx.redirectTo(),wx.switchTab(), wx.navigateBack(), wx.reLaunch()的区别
  * wx.navigateTo()：保留当前页面，跳转到应用内的某个页面。但是不能跳到 tabbar 页面
  * wx.redirectTo()：关闭当前页面，跳转到应用内的某个页面。但是不允许跳转到 tabbar 页面
  * wx.switchTab()：跳转到 abBar 页面，并关闭其他所有非 tabBar 页面
  * wx.navigateBack()：关闭当前页面，返回上一页面或多级页面。可通过 getCurrentPages() 获取当前的页面栈，决定需要返回几层
  * wx.reLaunch()：关闭所有页面，打开到应用内的某个页面
---

# session_id状态过期怎么办
---

# 正向代理和反向代理的区别
---

# 用过Nginx吗？都用过哪些？
nginx是一个高性能的HTTP和反向代理服务器。常使用场景： (1) 反向代理 (2) 网站负载均衡
---

# nginx跨域原理
---

# nginx的配置文件，它是怎么实现反向代理的
---

# 什么是死锁，产生死锁的原因及必要条件
  * 是指多个进程在运行过程中因争夺资源而造成的一种僵局，当进程处于这种僵持状态时，若无外力作用，它们都将无法再向前推进。举个例子来描述，如果此时有一个线程A，按照先锁a再获得锁b的的顺序获得锁，而在此同时又有另外一个线程B，按照先锁b再锁a的顺序获得锁。

  * 原因：
    - 竞争资源
      - 系统中的资源可以分为两类：
        1. 可剥夺资源，是指某进程在获得这类资源后，该资源可以再被其他进程或系统剥夺，CPU和主存均属于可剥夺性资源；
        2. 另一类资源是不可剥夺资源，当系统把这类资源分配给某进程后，再不能强行收回，只能在进程用完后自行释放，如磁带机、打印机等。
      - 产生死锁中的竞争资源之一指的是竞争不可剥夺资源（例如：系统中只有一台打印机，可供进程P1使用，假定P1已占用了打印机，若P2继续要求打印机打印将阻塞）
      - 产生死锁中的竞争资源另外一种资源指的是竞争临时资源（临时资源包括硬件中断、信号、消息、缓冲区内的消息等），通常消息通信顺序进行不当，则会产生死锁
    - 进程间推进顺序非法
      - 若P1保持了资源R1,P2保持了资源R2，系统处于不安全状态，因为这两个进程再向前推进，便可能发生死锁
      - 例如，当P1运行到P1：Request（R2）时，将因R2已被P2占用而阻塞；当P2运行到P2：Request（R1）时，也将因R1已被P1占用而阻塞，于是发生进程死锁

  * 4个必要条件
    1. 互斥条件：进程要求对所分配的资源进行排它性控制，即在一段时间内某资源仅为一进程所占用。
    2. 请求和保持条件：当进程因请求资源而阻塞时，对已获得的资源保持不放。
    3. 不剥夺条件：进程已获得的资源在未使用完之前，不能剥夺，只能在使用完时由自己释放。
    4. 环路等待条件：在发生死锁时，必然存在一个进程--资源的环形链。

  * 如何解决
    - 预防死锁：破坏4个必要条件中的一个或者多个来预防
      - 资源一次性分配：一次性分配所有资源，这样就不会再有请求了：（破坏请求条件）
      - 只要有一个资源得不到分配，也不给这个进程分配其他的资源：（破坏请保持条件）
      - 可剥夺资源：即当某进程获得了部分资源，但得不到其它资源，则释放已占有的资源（破坏不可剥夺条件）
      - 资源有序分配法：系统给每类资源赋予一个编号，每一个进程按编号递增的顺序请求资源，释放则相反（破坏环路等待条件）
    - 避免死锁：在资源动态分配的过程中，用某种方式防止系统进入不安全的状态
      - 银行家算法：首先需要定义状态和安全状态的概念。系统的状态是当前给进程分配的资源情况。因此，状态包含两个向量Resource（系统中每种资源的总量）和Available（未分配给进程的每种资源的总量）及两个矩阵Claim（表示进程对资源的需求）和Allocation（表示当前分配给进程的资源）。安全状态是指至少有一个资源分配序列不会导致死锁。当进程请求一组资源时，假设同意该请求，从而改变了系统的状态，然后确定其结果是否还处于安全状态。如果是，同意这个请求；如果不是，阻塞该进程知道同意该请求后系统状态仍然是安全的。
    - 检测死锁：运行时产生死锁，及时发现思索，将程序解脱出来
      - 首先为每个进程和每个资源指定一个唯一的号码；
      - 然后建立资源分配表和进程等待表。
    - 解除死锁：发生死锁后，撤销进程，回收资源，分配给正在阻塞状态的进程（解决方法如下）
      - 剥夺资源：从其它进程剥夺足够数量的资源给死锁进程，以解除死锁状态；
      - 撤消进程：可以直接撤消死锁进程或撤消代价最小的进程，直至有足够的资源可用，死锁状态.消除为止；所谓代价是指优先级、运行代价、进程的重要性和价值等。
---

# E2E 测试怎么做的，怎么保证测试覆盖率和准确性；
---

# 说一下单元测试、E2E测试？他们有什么区别？
  * 单元测试
    - 站在程序员角度的测试
    - 吧代码看成是一个个的组件，从而实现每一个组件的单独测试，测试内容主要是组件内每一个函数的返回结果是不是和期望值一样
  * e2e测试
    - 站在用户角度的测试
    - 不管你内部怎么实现的，我只负责打开浏览器，把测试内容在页面输入一遍，看是不是我想要的结果

  * 区别：单元测试程序员很容易检测自己是不是都正确。e2e是看需求是不是都正确的完成。
---

# hybrid 通信原理；
---

# 设计一个协同文档的技术流程；
---

# 介绍Oath2
---

# 怎么实现前端异常监控
  1. 错误的分类
    * 运行时报错：这种错误往往是写代码造成的。如语法、逻辑错误
    * 资源加载错误：这种错误通常是找不到文件或者文件加载超时造成的
  2. 错误捕获
    * 代码错误捕获
      - try...catch...
      - window.onerror
    * 资源加载错误
      - Object.onerror
  3. 错误上报
    * 常见的有ajax和image对象（推荐）
    * ajax上报就是在上文注释错误捕获的地方发起ajax请求，来向服务器发送错误信息
  4. 跨域js文件错误获取
    * 跨域文件获取是有限制的，如果想获取其他域下的js错误需要在script标签中添加crossorigin属性，然后服务器要设置header('Access-Control-Allor-Origin')
---

# 前端性能监控的工具有哪些，是怎么监控的？说一下见解
---

# 怎么捕获资源异常、同步异步的错误
---

# 前端错误收集（怎么记录，怎么区分是不是第三方插件的问题，怎么上报，怎么分析）
---

# 如何理解前后端分离架构？
---

# fetch原理 options
---

# fetch发送2次请求的原因
  > 因为你用fetch的post请求的时候，导致fetch 第一次发送了一个Options请求，询问服务器是否支持修改的请求头，如果服务器支持，则在第二次中发送真正的请求。
---

# axios和ajax的区别(ajax与fetch的区别）
  * 总结：axios是通过Promise实现对ajax技术的一种封装，就像jquery对ajax的封装一样，简单来说就是ajax技术实现了局部数据的刷新，axios实现了对ajax的封装，ajax有的axios都有，支持promise API，支持拦截请求和相应，支持自动转换为JSON数据，支持客户端支持防止CSRF/XSRF等。
---

# uni-app 的 h5 和 小程序打包出的文件有什么区别
---

# uniapp多端框架的多端编译原理讲一下
---

# uni-app和 vue 小程序有什么不一样
---

# 0.1+0.2为什么不等于0.3
---

# tab栏遇到ios的刘海屏怎么去解决
---

# serverless云开发适用于什么场景？有什么缺点？
---

# serverless和传统后台的区别，好处是什么
---

# webassembly是做什么的，适用于什么场景
---

# js对象和C++指针区别
---

# window.onerror能不能捕获异步的错误
---

# 如果catch中又有报错，onerror能不能捕获
---

# 怎么自己实现一个vue-cli
---

# 讲一讲threejs，它的兼容性怎么样
---

# 验证码怎么设置，生成验证码是在前端还是后端，在后端怎么做，在前端怎么做，怎么加密
---

# 手机扫码登录是怎么实现的，原理
  1. 每打开一次扫码页面会随机生成一个含有唯一ID的二维码
  2. 当用户使用扫码登陆后的来往扫描该二维码的时候，客户端会解析出二维码中的这个唯一ID会将这个id和手机上的来往账号及密码绑定，并上传到服务器；
  3. 来往网页版页面每隔1秒或2秒会get请求该id对应的来往账号及密码，如果id绑定上了来往账号和密码，那么就可以请求到账号和密码，就可以自动登陆了
---

# 数据库范式
---

# 数据库分表原则
---

# 详细说一下ARP协议，ARP病毒
---

# mogoodb v.s. mySql
---

# mySql事务
---

# 为什么用requestAnimationFrame来代替setTimeout
---

# 解释一下requestAnimationFrame
  1. 浏览器专门为DOM动画，canvas动画，SVG动画等等有一个统一的刷新机制
  2. 按帧对网页进行重绘，该方法告诉浏览器希望执行动画并请求浏览器在下一次重绘之前调用回调函数来更新动画
  3. 由系统来决定回调函数的执行时机，在运行时浏览器会自动优化方法的调用
---

# svg和canvas得区别，以及各自的优缺点
  * canvas: 
    1. 依赖分辨率
    2. 不支持事件处理器
    3. 弱的文本渲染能力
    4. 能够以 .png 或 .jpg 格式保存结果图像
    5. 最适合图像密集型的游戏，其中的许多对象会被频繁重绘

  * svg:
    1. 不依赖分辨率
    2. 支持事件处理器
    3. 最适合带有大型渲染区域的应用程序（比如谷歌地图）
    4. 复杂度高会减慢渲染速度（任何过度使用 DOM 的应用都不快）
    5. 不适合游戏应用
---

# canvas的width与height属性的值可不可以带单位？
不能
---

# canvas怎么解决图片和文字模糊的问题？
设置canvas的width和height为图片的原始尺寸，再设置css样式使得页面展示为正常尺寸。
---

# Bigint详解
---

# Vue项目是如何做部署的（你是用什么工具做支撑吗？还是直接传上去）
---

# eggjs中间件了解过吗
---

# 微信支付怎么做？说说流程
  1. 申请微信公众号及支付功能申请：根据公众号申请流程申请即可。 
  2. 获取商户支付配置信息及支付测试配置： 支付授权目录最多可以配置三个域名，测试授权目录只可以一个，这里需要 注意的是域名大小写必须要网站URL—致，否则会无法通过授权，提示支付请求的 URL不合法。另外，测试支付的微信号必须加到测试白名单，否则无法进行支付测 试。 
  3. H5页面发起支付请求，请求生成支付订单，获取用户授权（获取用户的openid) 
  4. 调用统一下单API，生成预付单 
  5. 生成JSAPI页面调用的支付参数并签名，注意时间戳timeStamp是32位字符串 
  6. 返回支付参数prepay—id,paySign参数的html文本给前端。 
  7. 微信浏览器自动调起支付JSAPI接口支付，提示用户输入密码。 
  8. 确认支付，输入密码，提交支付。 
  9. 步通知商户支付结果，商户收到通知返回确认信息。 
  10. 返回支付结果，并发微信消息提示。 
  11. 展示支付信息给用户，跳转到支付结果页面。
---

# 网站重构的理解
  * 重构：在不改变外部行为的前提下，简化结构、添加可读性，而在网站前端保持一致的行为。
    - 使网站前端兼容于现代浏览器(针对于不合规范的CSS、如对IE6有效的)
    -  对于移动平台的优化，针对于SEO进行优化
    -  减少代码间的耦合，让代码保持弹性
    -  压缩或合并JS、CSS、image等前端资源
---

# 10个资源放在一个域名下加载和放在多个域名下加载有什么区别？
  1. 更方便cdn缓存
  2. 突破浏览器并发限制
    * 在http1.x中，并发多个请求需要多个TCP连接，浏览器为了控制资源会有6个TCP连接的限制。10个同域名的资源，会并发6个请求，剩下4个排队等待；为了加快请求，会配置多域名
    * 在http2中，多路复用代理了1.x的序列和阻塞机制，所有的相同域名请求都通过同一个TCP连接并发完成
    * 10个同域名的资源，一桶并发请求
  3. 节省带宽
  4. 节省主域名连接数
---

# 怎么去设计一个组件封装
  * 组件封装的目的是为了重用,提高开发效率和代码质量
  * 低耦合,单一职责,可复用性,可维护性
---

# 微前端是什么, 有哪些特点和优势
---

# 微前端实现的主要原理
---

# 怎么解决样式隔离
---

# 如何解决主应用和子应用的隔离, 用 node.js 实现沙箱机制的原理
---

# 主应用修改了路由, 子应用如何感知到
---

# 计算机的原码、反码、补码
---

# 场景题：前端给页面加水印，说说各种编码的特点，说说数字签名的特点
---

# 场景题：实现协同编辑，说说你认为的技术关键点
---

# 32位和64位的区别？
---

# 为什么32位操作系统最大支持内存为4GB?
---