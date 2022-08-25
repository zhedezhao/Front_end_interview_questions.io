## 什么是 HTML？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ★ ☆ ☆ ☆
 HTML，全称是 HyperText Markup Language，即超文本标记语言，它不是编程语言，而是一种用来告知浏览器如何组织页面的标记语言，用来描述网页的表现，展示效果或功能及行为

* “超文本”（hybertext) 是指连接单个网站或多个网站网页的链接
* HTML 使用“标记”（markup) 来注明文本、图片和其它内容
* HTML 通过“标签”（tag）标记元素，标签由在<和>中包裹的元素名组成
* HTML 标签里的元素名不区分大小写。可以用大写、小写或混合形式书写

## 常用的浏览器引擎是什么 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ★ ★ ☆ ☆

浏览器是一种从 Web 获取和显示页面的程序，让用户通超链接访问更多页面

排版引擎（Layout Engine），也称为浏览器引擎（Browser Engine）、页面渲染引擎（Rendering Engine）或样板引擎，它是软件组件，负责获取标记式内容（如 HTML、XML 及图像文件等）和整理信息（如 CSS 及 XSL 等），并将排版后内容输出至显示器或打印机

常见的浏览器排版引擎分别是：

* Mozilla Firefox 使用 Gecko 引擎
* Apple Safari 和 早期 Google Chrome 使用 KDE 引擎，后发展成为 WebKit 引擎
* Internet Explorer 使用 Trident 引擎
* Microsoft Edge 早期使用 EdgeHTML 引擎
* Opera 早期使用 Presto 引擎
* 目前，Google Chrome 及基于 Chromium 浏览器，如 Microsoft Edge，Opera 使用基于 WebKit 分支自行构建的 Blink 引擎

## 请列举常用的 HTML 实体字符 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

字符 `<` `>` `"` `'` 和 `&` 等本身是 HTML 语法自身的特殊字符

表示其本身需要使用字符引用，即表示字符的特殊编码，每个字符引用以 & 开始，分号 ; 结束
原义字符 	等价字符引用
<!-- 
<thead>
<tr>
<th style="text-align:left"><strong>原义字符</strong></th>
<th style="text-align:left"><strong>等价字符引用</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">&lt;</td>
<td style="text-align:left">&amp;lt;</td>
</tr>
<tr>
<td style="text-align:left">&gt;</td>
<td style="text-align:left">&amp;gt;</td>
</tr>
<tr>
<td style="text-align:left">"</td>
<td style="text-align:left">&amp;quot;</td>
</tr>
<tr>
<td style="text-align:left">'</td>
<td style="text-align:left">&amp;apos;</td>
</tr>
<tr>
<td style="text-align:left">&amp;</td>
<td style="text-align:left">&amp;amp;</td>
</tr>
<tr>
<td style="text-align:left">空格</td>
<td style="text-align:left">&amp;nbsp;</td>
</tr>
</tbody> -->

## HTML 注释如何写 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

* HTML 注释使用特殊标记`<!--`和`-->`包裹
* HTML 注释不会被渲染
    * 会被传输
    * 解析时，早期 IE 浏览器使用 HTML 注释区分版本
    * 通常使用 `UglifyJS` 和 `Terser` 或正则匹配的方式，在生产环境删除注释
* HTML 注释用来描述
    * 代码是如何工作的
    * 不同部分代码做了什么

## 么是 HTML 语义化，有什么好处，一定要 HTML 语义化吗 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ★ ★ ★ ☆

语义是语言的含义，语义化是前端开发的专用术语，语义类标签是对内容的补充，表达标题摘要，文章结构、强调重点、丰富含义，避免歧义

HTML 语义化的好处包括

* 增强可读性，便于开发和维护

* 增强可访问性，便于屏幕阅读器定位和朗读

* 增强结构清晰度，利于 SEO
    HTML 语义化不是一定要执行的标准

* 利用无语义标签，如`<div>`和`<span>`可以满足几乎所有开发需求

* 可读性，可访问性和 SEO，使用语义化标签不是必须的

* 部分语义化标签存在兼容性问题，如 `<button>` 的默认 `type`不总为 submit 等

* 滥用列表标签，会增加不必要的嵌套，增加额外的 CSS Reset 的样式
    HTML 语义化以外，良好的命名，简明扁平的结构，良好的无障碍设计，清晰的导航和分区，一定程度上，也能弥补语义的欠缺，提升代码的机器阅读体验，降低抓取难度，提高索引权重

在明确知晓语义化标签的含义和组合搭配后，探索其使用的最佳实践和场景，而不是盲目地滥用、错用语义化标签，才能让 HTML 语义化标签体现更好的价值

## 连续空格如何渲染，意义是什么 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

* 为了代码的可读性，开发者通常会在 HTML 元素嵌套中使用空白
* 空白可以使用空格或 TAB 缩进实现
* HTML 解释器会将连续出现的空白字符减少为一个单独的空格符
* 如果一定要使用连续空格，可以使用全角空格或者实体字符 `&nbsp`;

## 如何声明文档类型 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ★ ☆ ☆ ☆

`<!DOCTYPE html> `是最简单有效的文档类型声明，目的是防止浏览器在渲染文档时，切换到“怪异模式（兼容模式）”。确保浏览器按照最佳相关规范进行渲染，而不是使用一个不符合规范的渲染

## 哪些字符集编码支持简体中文，如何解决 HTML 乱码问题 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ★ ☆ ☆ ☆

（1）支持简体中文的字符集编码

* GB 2312
    * 共收录 6763 个汉字，其中一级汉字 3755 个，二级汉字 3008 个，同时收录拉丁字母、希腊字母、日文平假名和片假名字母、俄语西里尔字母在内 682 个字符
    * 使用区位码“分区”，每区含有 94 个汉字 / 符号
        * 01 - 09 区为特殊符号
        * 16 - 55 区为一级汉字，按拼音排序
        * 56 - 87 区为二级汉字，按部署 / 笔画排序
    * 无法处理人名、古汉语中的罕用字和繁体字
* GBK
    * 汉字内码扩展规范
    * 拓展 GB 2312 - 80，拥有 23940 个码位，包括 21003 个汉字，883 个图形符号
    * 兼容 BG 2312 - 80，支持 希腊字母、俄语字母，不支持韩国字
* GB 18030
    * 国家标准 GB 18030 - 2005
    * 多字节编码，编码空间可定义 161 万个字元，包括 70244 个汉字
    * 完全兼容 GB 2312，基本兼容 GBK，支持少数民族文字、繁体汉字和日韩汉字
    BIG5
    * 大五码、五大码
    * 支持 13060 个中文文字
* Unicode
    * 万国码，国际码，统一码或单一码
    * 采用 ISO 10646 通用字符集，应用 UCS-2 使用 16 位编码空间，支持 65536 个字符
    * Unicode 转换格式即 UTF，UTF-8、UTF-16、UTF-32 是将数字转换到程序数据的编码方案
* UTF-8
    * 多字节编码，针对 Unicode 的可变长度字符编码
    * 使用 1 到 6 字节为每字符编码，实际最多 4 字节
        * 1 字节编码：ASCII 字符
        * 2 字节编码：带附加符号的拉丁文、希腊文、西里尔字母、亚美尼亚语、希伯来文、阿拉伯文、叙利亚文等字母
        * 3 字节编码：其他基本多文种平面（BMP）中字符（包含大部分常用字，汉字）
        * 4 字节编码：其他极少使用 Unicode 辅助平面的字符，如 Emoji 字符
* UTF-16
    * 介于 UTF-8 和 UTF-32 间，使用 2 字节或 4 字节存储，长度既固定又可变
* UTF-32
    * 固定长度的编码方案，不管字符编号大小，始终使用 4 字节存储
    * （2）如何解决 HTML 汉字乱码问题

HTML 汉字乱码的原因：

* 客户端不支持 HTML 编码的字符集

* 实际存储的字符集与使用 meta 标签声明的字符集不一致
    * 部分现代浏览器会自动纠正，根据实际使用的字符集编码渲染 HTML
        解决方法：

    * 建议使用 utf-8 存储并在页面添加 <meta charset="utf-8"> 声明编码类型

## 如何验证 HTML 是否正确 ？
##### 难度：★ ☆ ☆ ☆ ☆ 面试高频指数：★ ☆ ☆ ☆ ☆

验证 HTML 的最好方法使用 W3C 创立并维护的标记验证服务，网址如下：

https://validator.w3.org/

提交一个线上 URL，HTML 文件或者代码，网页会返回相应的错误报告

## 什么是 HTML5，HTML5 有哪些新特性 ？
##### 难度：★ ★ ★ ☆ ☆  面试高频指数：★ ★ ★ ★ ★

（1）什么是 HTML5？

HTML5 是定义 HTML 标准的组新版本，具有两个不同的概念：

* HTML5 是一个新版本的 HTML 语言，具有新的元素，属性和行为
* HTML5 有更大的技术集，允许构建多样化和更强大的网站和应用程序

（2）HTML5 有哪些新特性 ？

根据功能，HTML5 新特性可以分为：

* 语义：能够更恰当地描述内容是什么
    * 新的区块和段落元素
        * 举例：
            * `<section>` 表示一个包含在 HTML 文档的独立部分
            * `<article>` 表示文档、页面、应用或网站中的独立结构
            * `<nav>` 表示页面的一部分，其目的是在当前文档或其他文档提供导航链接
            * `<header>` 用于展示介绍性内容辅助导航。包含标题，Logo，搜索框和作者名称
            * `<footer>` 表示最近一个章节或根节点元素的页脚，包含作者，版权，相关链接
            * `<aside>` 表示一个和其余页面内容几乎无关的部分，通常是侧边栏或标注框
            * `<hgroup>`代表文档章节所属的多级别目录
        * 嵌入和允许操作新的多媒体内容
        * 举例：
            * `<audio>` 用于在文档中嵌入音频内容
            * `<video>` 用于再文档嵌入媒体播放器，支持视频及音频播放
    * 表单的改进
        * 强制性校验 API
            * 举例：
                * `required` 必填属性
                * `pattern` 声明正则校验规则属性
                * `minlength` 和 `maxlength` 限制输入的长度
                * `constraint validation API` 检测和自定义表单元素的状态
        * 新 `<input>` 元素的 `type` 属性值
            * 举例：
                * `color` 取色器
                * `date` 日期控件
                * `detetime-local` 不包括时区的日期控件
                * `month` 输入年和月的控件，没有时区
                * `range` 输入不需要精确地数字空间
                * `search` 搜索字符串的单行文字区域
                * `tel` 输入电话号码的控件
                * `time` 输入时间的控件
                * `url` 输入并校验 URL 的控件
    * 其它新的语义元素
        * 举例：
            * `<mark>` 为表示引用或符号目的而标记或突出显示的文本
            * `<figure>` 常与 `<figcaption>` 配合使用，表示独立的说明内容
            * `<data>` 将一个指定内容和机器可读的翻译联系在一起
            * `<time>` 表示机器可读的 24 小时制的时间或者公历日期
            * `<progress>` 显示一项任务的完成进度
            * `<meter>` 用来显示已知范围的标量值或者分数值
            * `<main>` 呈现了文档的 `<body>` 或应用的主体部分
            * `output` 表示计算或用户操作的结果
    * `<iframe>` 的改进
        * 精确控制 `<iframe>` 元素的安全级别和期望的渲染
        * 举例：
            * `sandbox` 对呈现在 `iframe` 框架中的内容启用一些额外的限制条件
            * `srcdoc` 支持的浏览器优先使用 `srcdoc` 代替 `src`
    * `MathML`
        * 用于描述数学公式、符号的一种标记语言，允许直接嵌入数学公式
* 连通性：能够通过创新的新技术方法进行通信
    * `Web Sockets`
        * 允许在页面和服务器之间建立持久连接，并通过这种方法来交换非 HTML 数据
    * `Server-sent events`
        * 允许服务器向客户端推送事件
    * `WebRTC`
        * 支持在浏览器客户端之间语音 / 视频交流和数据分享的技术
        * 浏览器原生支持点对点的分享应用数据和进行电话会议
* 离线 & 存储：能够让网页再客户端本地存储数据并且更高效地离线运行
    * 离线资源：应用程序缓存
        * 缓存 `.manifest` 上的资源，离线或资源没有更新时，浏览器会加载缓存的离线资源
    * 在线和离线事件
        * `navigator.onLine` 返回在线 `true` 或离线 `false`
        * `online` 和 `offline` 事件
            * `window` `document` `document.body` 使用 `addEventListener`
            * `document` `document.body` 的 `.ononline` 或 `.onoffline` 属性设为一个 JavaScript `Function` 对象
            * `<body>` 标签上指定 `ononline="..."` 或 `onoffline="..."` 属性
    * WHATWG 客户端会话和持久化存储（又名 DOM 存储）
        * `Storage`
            * DOM 存储被设计为用户提供一个更大存储量，更安全，更便捷的存储方法
            * 代替掉将一些不需要让服务器知道的信息存储到 `cookies` 里的这种传统方法
            * 构造函数 `Storage` 及其实例
                * `seesionStorage` 全局对象，维护着页面会话期间有效的存储空间，重新载入或从崩溃中恢复不会丢失
                * `localStorage` 全局对象，本次持久化存储，隐身模式下关闭浏览器会丢弃
    * `IndexedDB`
        * 用于在客户端存储大量的结构化数据，包括文件 / 二进制大型对象（blobs）
        * 使用索引实现对数据的高性能搜索
    * 在 Web 应用程序中使用文件
        * File API：可以访问 `FileList`，包含表示用户所选择的 `File` 对象
            * `name` 文件名称，只读字符串，只包含文件名，不包含任何路径信息
            * `size` 以字节数为单位的文件大小，只读的 64 位整数
            * `type` 文件的 MIME 类型，只读字符串，当类型不能确定为 ""
        * 通过 `change` 事件访问被选择的文件
            * `this.files`
        * 通过 `drogenter` `dragover` `drag` 的 `dataTransfer` 的 `files` 中获取文件列表
        * 对象 URL `window.URL.createObjectURL()` 和 `window.URL.revokeObjectURL()`
* 多媒体：加快普及 video 和 audio 应用，丰富 web 表现力
    * HTML5 音视频
        * `<video>` 和 `<audio>` 标签以及 JavaScript 和 APIs 用于对其进行控制
    * WebRTC
        * 支持在浏览器客户端之间语音 / 视频交流和数据分享的技术
        * 浏览器原生支持点对点的分享应用数据和进行电话会议
    * Camera API
        * 使用手机的摄像头拍照，然后把拍到的照片发送给当前网页
    * Track 和 WebVTT
        * `<track>` 元素怒被当作媒体元素 `<audio>` 和 `<video>` 的子元素
        * WebVTT（Web 视频文本跟踪格式）使用 `<track>` 元素现实定时文本轨道（如字幕或标题）的格式化，支持 `VTTCue` 和 `VTTRegion` 接口
* 2D/3D 绘图 & 效果：提供定制图形、动画界面的新选择
    * Canvas
        * `<canvas>` 元素被用来通过 JavaScript （Canvas API 或 WebGL API）绘制图形及图形动画
        * HTML5 文本 API 由 `<canvas>` 支持
            * `fillText(text, x, y, [, maxWidth])` 在指定的 (x, y) 位置填充指定的文本
            * `strokeText(text, x, y, [, maxWidth]` 在指定的 (x, y) 位置绘制文本边框
        * WebGL
            * WebGL （Web 图形库） 是一个 JavaScript API，可在任何兼容的 Web 浏览器中渲染高性能的交互式 3D 和 2D 图形，无需使用插件
                * WebGL 引入 OpenGL ES 2.0，通过 `canvas.getContext('webgl')` 使用
                * WebGL 2 引入 OpenGL ES 3.0，通过 `canvas.getContext('webgl2')` 使用
        * SVG
            * SVG （可缩放矢量图形）是一种描述二维的矢量图形，基于 XML 的标记语言
            * 优雅而简洁地渲染不同大小的图形，并和 CSS，DOM，JavaScript 和 SMIL 等其他网络标准无缝衔接
            * 可以搜索、索引、编写脚本和压缩，也可以使用任何文本编辑器和绘图软件来创建和编辑 SVG
* 性能 & 集成：提供作用显著的性能优化方案，更有效地使用设备硬件
    * Web Workers
        * 为 Web 内容在后台线程中运行脚本提供一种简单方法
        * 线程可以执行任务而不干扰用户界面
        * 专用 worker
            * `new Worker()` 构建
                通过 `postMessage()` 和 `onmessage` 事件函数发送和接收消息
        * 共享 worker
            * `new SharedWorker() `构建
            * 通过 ` port`.`postMessage()` 和 `port.onmessage` 事件函数发送和接收消息
                * worker 中需先使用 `onconnect `获取 `port`
    * XMLHttpRequest Level 2
        * 可以设置 HTTP 请求的时限
        * 可以使用 FormData 对象管理表单数据
        * 可以上传文件
        * 可以请求不同域名下的数据（跨域请求）
        * 可以获取服务器端的二进制数据
        * 可以获得数据传输的进度信息
    * 即时编译的 JavaScript 引擎
        * 新一代的 JavaScript 引擎更强大，性能更杰出
    * History API
        * History 接口允许操作浏览器的曾经在标签页或者框架里访问的会话历史记录
        * 属性
            * `History.length` 返回一个整数，该整数表示会话历史中元素的数目，包括当前加载的页
            * `History.scrollRestoration` 允许 Web 应用程序在历史导航上显式地设置默认滚动恢复行为。此属性可以是自动的（auto）或者手动的（manual）
            * `History.state` 返回一个表示历史堆栈顶部的状态的值。这是一种可以不必等待 `popstate` 事件而查看状态的方式
        * 方法
            * `History.back()` 在浏览器历史记录里前往上一页，用户可以点击浏览器左上角的返回按钮模拟此方法，等价于 `history.go(-1)`
            * `History.forward()` 在浏览器历史记录中前往下一页，用户可以点击浏览器左上角的前进按钮模拟此方法，等价于 `history.go(1)`
            * `History.go()` 通过当前页面的相对位置从浏览器历史记录（会话记录）加载页面
            * `History.pushState()` 按指定的名称和 URL（如果提供该参数）将数据 push 进会话历史栈，数据被 DOM 进行不透明处理，你可以指定任何可以被序列化的 JavaScript 对象
            * `History.replaceState()` 按指定的数据，名称和 URL（如果提供该参数）更新历史栈上最新的入口。这个数据被 DOM 进行了不透明处理。您可以指定任何可以被序列化的 JavaScript 对象
    * Content Editable
        * HTML 中任何元素都可以被编辑，设置 `contenteditable` 属性为 `true` 即可
        * HTML5 将此属性标准化
    * HTML 拖放 API
        * HTML 拖放（Drag and Drop）接口使应用程序能够在浏览器中私用拖放功能
        * 引入拖放功能的基本步骤
            * 确定可拖拽元素
                * 给元素添加 `draggable` 属性，添加全局事件处理函数 `ondragstart`
                定义拖拽数据
                * 通过 `drag event` 的 `dataTransfer` 属性访问事件数据
                * 通过 `dataTransfer `的 `setData()` 方法为拖拽数据添加一个项
                * 通过 `dataTransfer `的 `setDrageImage` 方法定义拖拽图像
                * 通过 `dataTransfer `的 `dropEffect` 属性定义拖拽效果
                    * `copy `表明拖拽的数据将从它原本的位置拷贝到目标的位置
                    * `move` 表明被拖拽的数据将被移动
                    * `link` 表明拖拽源位置和目标之间将会创建一些关系表格或是连接
            * 确定放置区域
                * 给元素添加 `ondragover` 和 `ondrop` 事件处理程序属性
            * 定义放置效果
                * 通过 `dataTransfer `的 `dropEffect` 属性定义拖拽效果
            * 拖拽结束
                * 拖拽操作结束时，在源元素（开始拖拽时的目标元素）上触发 dragend 事件
                * 不管拖拽是完成还是取消，这个事件都会被触发
    * HTML 焦点管理
        * DOM 属性 `activeElement` 与方法 `hasFocus()` 为程序按提供了更好的控制页面交互的能力，特别是丢与用户行为引发的交互
            * `activeElement` 只读属性，用来返回当前在 DOM 或者 shadow DOM 树中处于聚焦状态的 `Element`
            * ```Do``cumen``t.hasFocus()``` 方法返回一个 Boolean，表明当前文档或者文档内的节点是否获得了焦点。该方法可以用来判断当前文档中的活动元素是否获得了焦点
        * 两者关系
            * 获得焦点的元素一定是当前文档的活动元素
            * 一个文档中的活动元素不一定获得了焦点
    * 基于 Web 的协议处理程序
        * 使用 `navigator.registerProtoolHandler(scheme,url, title)` 方法把 web 应用程序注册成一个协议处理程序
    * requestAnimationFrame
        * 传入一个回调函数，该回调函数会在浏览器下一次重绘之前执行
    * 全屏 API
        * `全屏 API` 为使用用户的整个屏幕展现网络内容提供了一种简单的方式，不需要时退出全屏模式
        * 方法
            * `Document.exitFullscreen()` 用于请求从全屏模式切换到窗口模式，会返回一个 `Promise`，会在全屏模式完全关闭的时候，被重置为 `resolved` 状态
            * `Element.requestFullscreen()` 请求浏览器将特定元素置为全屏模式，隐去屏幕上的浏览器所有 UI 元素，以及其它应用
        * 属性
            * `DocumentOrShadowRoot.fullscreenElement` `fullscreenElement` 属性提供了当前在 DOM（或者 shadow DOM）里被展示为全屏模式的 `Element`，如果这个值为 `null`，文档不处于全屏模式
            * `Document.fullscreenEnabled` `fullscreenEnabled` 属性提供了启用全屏模式的可能性。当它的值是 `false` 的时候，表示全屏模式不可用
        * 事件处理程序
            * Document 事件处理程序 `onfullscreenchange` 和 `onfullscreenerror`
            * Element 事件处理程序 `onfullscreenchange` 和 `onfullscreenerror`
    * 指针锁定 API
        * 光标移到浏览器或者屏幕区域之外，指针锁定也能够让你访问鼠标事件
        * 指针锁定是持久性的。指针锁定不释放鼠标，直到作出一个显式的 API 调用或者用户使用一个专门的释放手势
        * 指针锁定不局限于浏览器或者屏幕边界
        * 指针锁定持续发送事件，而不管鼠标按钮状态如何
        * 指针锁定隐藏光标
        * 指针锁定目前需要先进入全屏模式 `requestFullscreen()` 然后执行 `requestPointerLock()` 方法
    * 在线和离线事件
        * `navigator.onLine` 返回在线 `true` 或离线 `false`
        * `online` 和 `offline` 事件
            * `window` `document` `document.body` 使用 `addEventListener`
            * `document` `document.body` 的 `.ononline` 或 `.onoffline` 属性设为一个 JavaScript `Function` 对象
            * `<body>` 标签上指定 `ononline="..."` 或 `onoffline="..."` 属性
* 设备访问 ：能够处理各种输入和输出设备
    * Camera API
        * 使用手机的摄像头拍照，然后把拍到的照片发送给当前网页
    * 触摸事件
        * 触摸事件提供了在触摸屏或触控板商解释手指（或触控笔）活动的能力
        * 触摸事件接口可为程序提供多点触控交互的支持，分为开始、移动、结束三个阶段
        * 接口
            * `TouchEvent` 接口将当前所有活动的触摸点封装起来
            * `Touch` 接口表示单独一个触摸点，其中包括浏览器视角的相对坐标
            * `TouchList` 表示一组 `Touch`，用于多点触控的情况
    * 使用地理位置定位
        * 地理位置 API 允许用户向 Web 应用程序提供他们的位置
        * 出于隐私考虑，报告地理位置和前会先请求用户许可
        * 方法，通过 `navigator.geolocation` 提供
            * `getCurrentPosition(success[, error[, options]])` 用来获取设备当前位置
            * `watchPosition(success[, error, options]])` 用于注册监听器，在设备的地理位置发生改变的时候自动被调用，返回一个 `id`
            * `clearWatch(id)` 清除注册的位置及错误监听器
    * 检测设备方向
        * `DeviceOrientationEvent` 它会在加速度传感器检测到设备在方向上产生变化时触发
        * `DeviceMotionEvent` 它会在加速度发生改变时触发
    * 指针锁定 API
        * 光标移到浏览器或者屏幕区域之外，指针锁定也能够让你访问鼠标事件
        * 指针锁定是持久性的。指针锁定不释放鼠标，直到作出一个显式的 API 调用或者用户使用一个专门的释放手势
        * 指针锁定不局限于浏览器或者屏幕边界
        * 指针锁定持续发送事件，而不管鼠标按钮状态如何
        * 指针锁定隐藏光标
        * 指针锁定目前需要先进入全屏模式 `requestFullscreen()` 然后执行 `requestPointerLock()` 方法
* 样式设计：支持创作更复杂的主题

## 什么是 MIME types，常见的 MIME types 有哪些 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

MIMEtype（现在称为“媒体类型（media type）”，但有时也是“内容类型”（content type））是指示文件类型的字符串，与文件一起发送（例如，一个声音文件可能被标记为 `audio/ogg` 一个图像文件可能是 `image/png` ）。它与传统 Windows 上的文件扩展名有相同目的

`NavigatorPlugins.mimeTypes` 返回一个 `MimeTypeArray` 对象，其中包含可被当前浏览器识别的 `MimeType` 对象列表

两种主要的 MIME 类型

`text/plain` 表示文本文件的默认值，一个文本文件应当是人类可读的，并且不包含二进制数据

`application/octet-stream` 表示所有其他情况的默认值。一种未知的文件类型应当使用此类型。浏览器在处理这些文件时会特别小心，试图防止、避免用户的危险行为

Web 常见的 MIME 类型


<!-- <thead>
<tr>
<th style="text-align:left"><strong>扩展名</strong></th>
<th style="text-align:left"><strong>文档类型</strong></th>
<th style="text-align:left"><strong>MIME 类型</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">.aac</td>
<td style="text-align:left">AAC audio</td>
<td style="text-align:left">audio/aac</td>
</tr>
<tr>
<td style="text-align:left">.abw</td>
<td style="text-align:left">AbiWord document</td>
<td style="text-align:left">application/x-abiword</td>
</tr>
<tr>
<td style="text-align:left">.arc</td>
<td style="text-align:left">Archive document</td>
<td style="text-align:left">application/x-freearc</td>
</tr>
<tr>
<td style="text-align:left">.avi</td>
<td style="text-align:left">Audio Video Interleave</td>
<td style="text-align:left">video/x-msvideo</td>
</tr>
<tr>
<td style="text-align:left">.azw</td>
<td style="text-align:left">Amazon Kindle eBook format</td>
<td style="text-align:left">application/vnd.amazon.ebook</td>
</tr>
<tr>
<td style="text-align:left">.bin</td>
<td style="text-align:left">Any kind of binary data</td>
<td style="text-align:left">application/octet-stream</td>
</tr>
<tr>
<td style="text-align:left">.bmp</td>
<td style="text-align:left">Windows OS / 2 Bitmap Graphics</td>
<td style="text-align:left">image/bmp</td>
</tr>
<tr>
<td style="text-align:left">.bz</td>
<td style="text-align:left">BZip archive</td>
<td style="text-align:left">application/x-bzip</td>
</tr>
<tr>
<td style="text-align:left">.bz2</td>
<td style="text-align:left">BZip2 archive</td>
<td style="text-align:left">application/x-bzip2</td>
</tr>
<tr>
<td style="text-align:left">.csh</td>
<td style="text-align:left">C-Shell script</td>
<td style="text-align:left">application/x-csh</td>
</tr>
<tr>
<td style="text-align:left">.css</td>
<td style="text-align:left">Cascading Style Sheets</td>
<td style="text-align:left">text/css</td>
</tr>
<tr>
<td style="text-align:left">.csv</td>
<td style="text-align:left">Comma-separated values</td>
<td style="text-align:left">text/csv</td>
</tr>
<tr>
<td style="text-align:left">.doc</td>
<td style="text-align:left">Microsoft Word</td>
<td style="text-align:left">application/msword</td>
</tr>
<tr>
<td style="text-align:left">.docx</td>
<td style="text-align:left">Microsoft Word（OpenXML）</td>
<td style="text-align:left">application/vnd.openxmlformats-officedocument.wordprocessingml.document</td>
</tr>
<tr>
<td style="text-align:left">.eot</td>
<td style="text-align:left">MS Embedded OpenType fonts</td>
<td style="text-align:left">application/vnd.ms-fontobject</td>
</tr>
<tr>
<td style="text-align:left">.epub</td>
<td style="text-align:left">Electronic publication（EPUB）</td>
<td style="text-align:left">application/epub+zip</td>
</tr>
<tr>
<td style="text-align:left">.gif</td>
<td style="text-align:left">Graphics Interchange Format（GIF）</td>
<td style="text-align:left">image/gif</td>
</tr>
<tr>
<td style="text-align:left">.htm<br>.html</td>
<td style="text-align:left">HyperText Markup Language（HTML）</td>
<td style="text-align:left">text/html</td>
</tr>
<tr>
<td style="text-align:left">.ico</td>
<td style="text-align:left">Icon format</td>
<td style="text-align:left">image/vnd.microsoft.icon</td>
</tr>
<tr>
<td style="text-align:left">.ics</td>
<td style="text-align:left">iCalendar format</td>
<td style="text-align:left">text/calendar</td>
</tr>
<tr>
<td style="text-align:left">.jar</td>
<td style="text-align:left">Java Archive（JAR）</td>
<td style="text-align:left">application/java-archive</td>
</tr>
<tr>
<td style="text-align:left">.jpeg<br>.jpg</td>
<td style="text-align:left">JPEG images</td>
<td style="text-align:left">image/jpeg</td>
</tr>
<tr>
<td style="text-align:left">.js</td>
<td style="text-align:left">JavaScript</td>
<td style="text-align:left">text/javascript</td>
</tr>
<tr>
<td style="text-align:left">.json</td>
<td style="text-align:left">JSON format</td>
<td style="text-align:left">application/json</td>
</tr>
<tr>
<td style="text-align:left">.jsonld</td>
<td style="text-align:left">JSON-LD format</td>
<td style="text-align:left">application/ld+json</td>
</tr>
<tr>
<td style="text-align:left">.mid<br>.midi</td>
<td style="text-align:left">Musical Instrument Digital Interface（MIDI）</td>
<td style="text-align:left">audio/midi<br>audio/x-midi</td>
</tr>
<tr>
<td style="text-align:left">.mjs</td>
<td style="text-align:left">JavaScript module</td>
<td style="text-align:left">text/javascript</td>
</tr>
<tr>
<td style="text-align:left">.mp3</td>
<td style="text-align:left">MP3 Audio</td>
<td style="text-align:left">audio/mpeg</td>
</tr>
<tr>
<td style="text-align:left">.mpeg</td>
<td style="text-align:left">MPEG Video</td>
<td style="text-align:left">video/mpeg</td>
</tr>
<tr>
<td style="text-align:left">.mpkg</td>
<td style="text-align:left">Apple Installer Package</td>
<td style="text-align:left">application/vnd.apple.installer+xml</td>
</tr>
<tr>
<td style="text-align:left">.odp</td>
<td style="text-align:left">OpenDocument presentation document</td>
<td style="text-align:left">application/vnd.oasis.opendocument.presentation</td>
</tr>
<tr>
<td style="text-align:left">.ods</td>
<td style="text-align:left">OpenDocument<br>spreadsheet document</td>
<td style="text-align:left">application/vnd.oasis.opendocument.spreadsheet</td>
</tr>
<tr>
<td style="text-align:left">.odt</td>
<td style="text-align:left">OpenDcoument text document</td>
<td style="text-align:left">application/vnd.oasis.opendocument.text</td>
</tr>
<tr>
<td style="text-align:left">.oga</td>
<td style="text-align:left">OGG audio</td>
<td style="text-align:left">audio/ogg</td>
</tr>
<tr>
<td style="text-align:left">.ogv</td>
<td style="text-align:left">OGG video</td>
<td style="text-align:left">video/ogg</td>
</tr>
<tr>
<td style="text-align:left">.ogx</td>
<td style="text-align:left">OGG</td>
<td style="text-align:left">application/ogg</td>
</tr>
<tr>
<td style="text-align:left">.otf</td>
<td style="text-align:left">OpenType font</td>
<td style="text-align:left">font/otf</td>
</tr>
<tr>
<td style="text-align:left">.png</td>
<td style="text-align:left">Portable Network Graphics</td>
<td style="text-align:left">image/png</td>
</tr>
<tr>
<td style="text-align:left">.pdf</td>
<td style="text-align:left">Adobe Portable Document Format（PDF）</td>
<td style="text-align:left">application/pdf</td>
</tr>
<tr>
<td style="text-align:left">.ppt</td>
<td style="text-align:left">Microsoft PowerPoint</td>
<td style="text-align:left">application/vnd.ms-powerpoint</td>
</tr>
<tr>
<td style="text-align:left">.pptx</td>
<td style="text-align:left">Microsoft PowerPoint（OpenXML）</td>
<td style="text-align:left">application/vnd.openxmlformats-officedocument.presentationml.presentation</td>
</tr>
<tr>
<td style="text-align:left">.rar</td>
<td style="text-align:left">RAR archive</td>
<td style="text-align:left">application/x-rar-compressed</td>
</tr>
<tr>
<td style="text-align:left">.rtf</td>
<td style="text-align:left">Rich Text  Format（RTF）</td>
<td style="text-align:left">application/rtf</td>
</tr>
<tr>
<td style="text-align:left">.sh</td>
<td style="text-align:left">Boume shell script</td>
<td style="text-align:left">application/x-sh</td>
</tr>
<tr>
<td style="text-align:left">.svg</td>
<td style="text-align:left">Scalable Vector Graphics（SVG）</td>
<td style="text-align:left">image/svg+xml</td>
</tr>
<tr>
<td style="text-align:left">.swf</td>
<td style="text-align:left">Small web format（SWF）or Adobe Flash document</td>
<td style="text-align:left">application/x-shockwave-flash</td>
</tr>
<tr>
<td style="text-align:left">.tar</td>
<td style="text-align:left">Tape Archive（TAR）</td>
<td style="text-align:left">application/x-tar</td>
</tr>
<tr>
<td style="text-align:left">.tif<br>.tiff</td>
<td style="text-align:left">Tagged Image File Format（TIFF）</td>
<td style="text-align:left">image/tiff</td>
</tr>
<tr>
<td style="text-align:left">.ttf</td>
<td style="text-align:left">TrueType Font</td>
<td style="text-align:left">font/ttf</td>
</tr>
<tr>
<td style="text-align:left">.txt</td>
<td style="text-align:left">Text</td>
<td style="text-align:left">text/plain</td>
</tr>
<tr>
<td style="text-align:left">.vsd</td>
<td style="text-align:left">Microsoft Visio</td>
<td style="text-align:left">application/vnd.visio</td>
</tr>
<tr>
<td style="text-align:left">.wav</td>
<td style="text-align:left">Waveform Audio Format</td>
<td style="text-align:left">audio/wav</td>
</tr>
<tr>
<td style="text-align:left">.weba</td>
<td style="text-align:left">WEBM audio</td>
<td style="text-align:left">audio/webm</td>
</tr>
<tr>
<td style="text-align:left">.webm</td>
<td style="text-align:left">WEBM video</td>
<td style="text-align:left">video/webm</td>
</tr>
<tr>
<td style="text-align:left">.webp</td>
<td style="text-align:left">WEBP image</td>
<td style="text-align:left">image/webp</td>
</tr>
<tr>
<td style="text-align:left">.woff</td>
<td style="text-align:left">Font  Format（WOFF）</td>
<td style="text-align:left">font/woff</td>
</tr>
<tr>
<td style="text-align:left">.woff2</td>
<td style="text-align:left">Web Open Font Format（WOFF）</td>
<td style="text-align:left">font/woff2</td>
</tr>
<tr>
<td style="text-align:left">.xhtml</td>
<td style="text-align:left">XHTML</td>
<td style="text-align:left">application/xhtml+xml</td>
</tr>
<tr>
<td style="text-align:left">.xls</td>
<td style="text-align:left">Microsoft Excel</td>
<td style="text-align:left">application/vnd.ms-excel</td>
</tr>
<tr>
<td style="text-align:left">.xlsx</td>
<td style="text-align:left">Microsoft Excel（OpenXML）</td>
<td style="text-align:left">application/vnd.openxmlformats-officedocument.spreadsheetml.sheet</td>
</tr>
<tr>
<td style="text-align:left">.xml</td>
<td style="text-align:left">XML</td>
<td style="text-align:left">application/xml 代码对普通用户来说不可读<br>text/xml 代码对普通用户来说可读</td>
</tr>
<tr>
<td style="text-align:left">.xul</td>
<td style="text-align:left">XUL</td>
<td style="text-align:left">application/vn.mozila.xul+xml</td>
</tr>
<tr>
<td style="text-align:left">.zip</td>
<td style="text-align:left">ZIP archive</td>
<td style="text-align:left">application/zip</td>
</tr>
<tr>
<td style="text-align:left">.3gp</td>
<td style="text-align:left">3GPP<br>audio/video container</td>
<td style="text-align:left">video/3gpp<br>audio/3gpp</td>
</tr>
<tr>
<td style="text-align:left">.3g2</td>
<td style="text-align:left">3GPP2<br>audieo/video container</td>
<td style="text-align:left">video/3gpp2<br>audio/3gpp2</td>
</tr>
<tr>
<td style="text-align:left">.7z</td>
<td style="text-align:left">7-zip archive</td>
<td style="text-align:left">application/x-7z-compressed</td>
</tr>
</tbody> -->

## 什么是 ARIA？
##### 难度：★ ★ ★ ☆ ☆  面试高频指数：★ ★ ★ ★ ★

ARIA（Accessible Rich Internet Applications）是能够让残障人士更加便利地访问 Web 内容和使用 Web 应用的一套机制，来自 W3C 的网络无障碍计划（Web Accessibility Initiative）

* ARIA 是对超文本标记语言（HTML）的补充，以便在没有其他机制的情况下，使得应用程序中常用的交互和小部件可以传递给辅助交互技术
* ARIA 是一组特殊的易用性属性，可以添加到任意标签上，尤其适用于 HTML。role 属性定义了对象的通用类型（例如文章、警告、或幻灯片）。额外的 ARIA 属性提供了其他有用的特性，例如表单的描述或进度条的当前值
* ARIA 在大多数流行的浏览器和屏幕阅读器中得到了实现
* 开发人员应该更倾向使用对应的语义化 HTML 元素，而不是使用 ARIA

# 元素
## 什么是 HTML 标签 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

* HTML 超文本标记语言标记标签通常被称为 HTML 标签
* HTML 标签是 HTML 语言中最基本单位和重要组成部分
* HTML 标签不区分大小写，从一致性、可读性等方面来说，最好仅使用小写字母
* HTML 标签以尖括号（ `<` `>` ）开始和结束
    * 通常成对出现，分别是开始标签和结束标签，也可以称为开放标签和闭合标签
    * 自闭合标签只有其本身，在开始标签中自动闭合

## HTML 标签区分大小写吗 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

* HTML 标签不区分大小写
    * 输入标签时，既可以使用大写字母，也可以使用小写字母
* 从一致性、可读性等方面来说，最好仅使用小写字母

## 什么是 HTML 元素 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

HTML 元素是指从开始标签到结束标签的所有代码

* 开始标签：包含元素的名称，被左、右角括号所包围。表示元素从这里开始或者开始起作用
* 结束标签：与开始标签相似，只是其在元素名之前包含了一个斜杠，表示着元素的结尾
* 内容：元素的内容
* 元素：开始标签、结束标签与元素相结合，便是一个完整的元素

## HTML 元素有哪些分类方法 ？
##### 难度：★ ★ ☆ ☆ ☆  面试高频指数：★ ★ ☆ ☆ ☆

* 按闭合特征分类
    * 双标签元素：开始标签和结束标签成对，中间包括内容
    * 单标签元素：空元素，开始标签自动闭合，没有内容
* 按显示方式分类
    * 行内元素（内联元素）
        * 只占据它对应标签的边框所包含的空间
        块级元素
        * 占据其父元素（容器）的整个空间
        * 通常浏览器会在块级元素前后另起一行
        * 块级元素可以包含行内元素和其他块级元素
* 按 HTML5 规范文档（HTML-conformant document）分类
    * 主内容类：描述了很多元素共享的内容规范
        * 元数据内容（Metadata content）：此类元素修改文档的其余部分的陈述或者行为，建立与其他文档的链接，或者传达其他外带信息
            * 举例： `<base>` `<link>` `<meta>` `<noscript>` `<script>` `<style>` `<title>`
        * 流式元素（Flow content）：此类元素同行包含文本或植入的内容
            * 举例：   `<a>` `<abbr>` `<address>` `<article>` `<aside>` `<audio>` `<b>` `<bdo>` `<bdi>` `<blockquote>` `<br>` `<button>` `<canvas>` `<cite>` `<code>` `<data>` `<datalist>` `<del>` `<details>` `<dfn>` `<div>` `<dl>` `<em>` `<embed>` `<fieldset>` `<figure>` `<footer>` `<form>` `<h1>` `<h2>` `<h3>` `<h4>` `<h5>` `<h6>` `<header>` `<hgroup>` `<hr>` `<i>` `<iframe>` `<img>` `<input>` `<ins>` `<kbd>` `<label>` `<main>` `<map>` `<mark>` `<math>` `<menu>` `<meter>` `<nav>` `<noscript>` `<object>` `<ol>` `<output>` `<p>` `<pre>` `<progress>` `<q>` `<ruby>` `<s>` `<samp>` `<script>` `<section>` `<select>` `<small>` `<span>` `<strong>` `<sub>` `<sup>` `<svg>` `<table>` `<template>` `<textarea>` `<time>` `<ul>` `<var>` `<video>` `<wbr>`  等和 Text
            * 以下元素仅限于某种特殊情况，属于此类
                * `<area>` 仅限于它作为 `<map>` 的子元素时
                * `<link>` 仅限于 `itemprop` 属性存在的情形
                * `<meta>` 仅限于 `itemprop` 属性存在的情形
                * `<style>` 仅限于 `scoped` 属性存在的情形
        * 章节元素（Heading content）：隶属于分节内容模型的元素，再当前的大纲中创建一个分节。此分节将定义 <`header>` 元素、 `<footer>` 元素和标题元素的范围
            * 举例： `<article>` `<aside>` `<nav>` 和 `<section>`
        * 标题元素（Heading content）：定义了分节的标题，而这个分节可能由一个明确的分节内容元素直接标记，也可能由标题本身隐式地定义
            * 举例： `<h1>` - `<h6>` 和 `<hgroup>`
        * 短语元素（Phrasing content）：规定文本和它包含的标记，一些短语元素构成段落
            * 举例：   `<abbr>` `<audio>` `<b>` `<bdo>` `<br>` `<button>` `<canvas>` `<cite>` `<code>` `<datalist>` `<dfn>` `<em>` `<embed>` `<i>` `<iframe>` `<img>` `<input>` `<kbd>` `<label>` `<mark>` `<math>` `<meter>` `<noscript>` `<object>` `<output>` `<progress>` `<q>` `<ruby>` `<samp>` `<script>` `<select>` `<small>` `<span>` `<strong>` `<sub>` `<sup>` `<svg>` `<textarea>` `<time>` `<var>` `<video>` `<wbr>` 和 plain text
            * 以下元素仅限于某种特殊情况，属于此类
                * `<a>` 仅限于它包含 phrasing content 时
                * `<area>` 仅限于它作为 `<map>` 的子元素时
                * `<del>` 仅限于它包含 phrasing content 时
                * `<ins>` 仅限于它包含 phrasing content 时
                * `<link>` 仅限于 `itemprop` 属性存在的情形
                * `<map>` 仅限于它包含 phrasing content 时
                * `<meta>` 仅限于 `itemprop` 属性存在的情形
        * 嵌入元素（Embedded content）：输入另一个资源或者将来自另一种标记语言或命名空间的内容插入到文档中
            * 举例： `<audio>` `<canvas>` `<embed>` `<iframe>` `<img>` `<math>` `<object>` `<svg>` `<video>`
            交互元素（Interactive content）：交互式内容包含为用户交互而特别设计的元素
            * 举例： `<a>` `<button>` `<details>` `<embed>` `<iframe>` `<label>` `<select>` 和 `<textarea>`
            * 以下元素仅限于某种特殊情况，属于此类
                * `<audio>` 仅限于 `controls` 属性存在
                * `<img>` 仅限于 `usemap` 属性存在
                * `<input>` 仅限于 `type` 属性不处于隐藏（hidden）状态
                * `<menu>` 仅限于 `type` 属性处于工具栏（toolbar）状态
                * `<object>` 仅限于 `usemap` 属性存在
                * `<video>` 仅限于 `controls` 属性存在
    * 表单相关内容类：描述了表单相关元素共有的内容规范
        * 可列举的元素（listed）
            * 举例： `<button>` `<fieldset>` `<input>` `<object>` `<output>` `<select>` 和 `<textarea>`
        * 可标签的元素（labelable）
            * 可以和 `<label>` 相关联的元素
            * 举例： `<button>` `<input>` `<meter>` `<output>` `<progress>` `<select>` 和 `<textarea>`
        * 可提交的元素（submittable）
            * 包括当表单提交时，可以用来组成表单数据的元素
            * 举例： `<button>` `<input>` `<object>` `<select>` 和 `<textarea>`
        * 可重置的元素（resettable）
            * 当表单重置时会被重置的元素
            * 举例： `<input>` `<output>` `<select>` 和 `<textarea>`
    * 特殊内容类：描述了仅在某些特殊元素商才需要遵守的规范，通常这些元素都有特殊的上下文关系
        * 支持脚本元素：不会直接渲染输出在页面文档中。被用来存放脚本代码及脚本代码所要用到的数据
            * 举例： `<script>` `<template>`
        * 透明内容模型元素（Transparent content model）
            * 如果一个元素拥有透明内容模型，将透明标签删除，依然是合法的 HTML5 元素
            * 举例： `<del>` `<ins>`

## 什么是 HTML 头部元素 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

HTML 头部元素，即 `<head>` 元素

* HTML 头部元素的内容不会在浏览器中显示
* HTML 头部元素的作用是保存页面的标题、元数据

## 什么是元数据 ？
###### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

* 元数据（Metadata），简单的来说就是描述数据的数据
* HTML 文件在头部元素，即 `<head>` 标签中包含描述该文档的元数据
* HTML 元数据通常使用 `<meta>` 标签表示，共有 4 种类型
    * 如果设置了 `name` 属性
        * `meta` 元素提供的是文档级别（document-level）的元数据，应用于整个页面
        * `meta` 指定了元素的类型，说明该元素包含了什么类型的信息
        * 与 `content` 一起使用，后者指定实际的元数据内容，用来添加 `author` `description` 用于提交作者、摘要和 SEO
    * 如果设置了 `http-equiv` 属性
        * `meta` 元素则是编译指令，提供的信息与类似命名的 HTTP 头部相同
        * `content-security-policy`
            * 允许页面作者定义当前页的内容策略
            * 指定允许的服务器源和脚本，有助于防止跨站点脚本攻击（XSS）
        * `content-type`
            * 用于声明文档类型，如 `text/html; charset=utf-8`
        * `default-style`
            * 设置默认 CSS 样式表组的名称
            * `content` 属性的值必须匹配同一文档中一个 `link` 元素上的 `title` 属性的值
        * `x-ua-compatible`
            * `content` 属性必须为 `IE=edge`
        * `refresh`
            * `content` 只包含一个正整数，则为重新载入页面的时间间隔（秒）
            * `content` 包含一个正整数，并且后面跟着字符串 `;ulr=` 和一个合法的 URL，则是重定向到指定链接的时间间隔（秒）
    * 如果设置了 `charset` 属性，
        * `meta` 元素是一个字符集声明，告诉文档使用哪种字符编码
        * 值与 ASCII 大小写（ASCII case-insensitive）无关，如 `utf-8`
        * 如果设置了 `itemprop` 属性，`meta` 元素提供用户定义的元数据
        * `content` 属性对应用户定义的值，可用于数据标记和结构化数据提交
        * `property` 属性通常与 `itemprop`作用一致，如 Facebook 编写的元数据协议（Open Graph protocol）使用 `property` 声明属性名

## 什么是 Open Graph protocol？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

元数据协议（Open Graph Data）由 Facebook 编写制定的 Metatags 规格，用来标注页面

* 帮助社交媒体、搜索引擎高效、准确地获取网页的标题、主图及元数据
* 使得网页在社交分享及搜索结果中有更好的展现
* 除网页外，还可以用于声明将音乐、视频、文章、书籍、用户信息等转换为图形对象
* 应用元数据协议，需要在页面添加 `<meta>` 标签放在网页的 `<head>` 中，其中包括：

基本元数据

* og:title - 标题

* og:type - 对象类型

* og:image - 图像 URL

* og:url - 对象 URL
* 可选元数据

* og:audio - 音频文件 URL

* og:description - 描述

* og:determiner - 出现在对象标题前的单词，可选 a / an / the / auto，默认为空

* og:locale - 语言环境，格式为 language_TERRITORY，默认为 en_US

* og:locale:alternate - 页面可用的其他语言环境数组

* og:site_name - 网站名称，如 Facebook

* og:video - 视频 URL
    结构化属性

某些属性可以附加额外的元数据

* og:image
    * og:image:url - 图像 URL
    * og:image:secure_url - HTTPS 下的图像 URL
    * og:image:type - 图像 MIME 类型
    * og:image:width - 图像宽度
    * og:image:height - 图像高度
    * og:image:alt - 图像内容描述（不是标题）
* og:video
    * og:video:url - 视频 URL
    * og:video:secure_url - HTTPS 下的视频 URL
    * og:video:type - 视频 MIME 类型
    * og:video:width - 视频宽度
    * og:video:height - 视频高度
* og:audio
    * og:audio:url - 音频 URL
    * og:audio:secure_url - HTTPS 下的音频 URL
    * og:audio:type - 音频 MINE 类型


## 给页面添加标题，都有哪些最佳实践 ？
##### 难度：★ ★ ★ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

页面标题通过 `<title>` 定义文档的标题

* 显示在浏览器的标题栏或者标签页

* 只包含文本，若是包含有标签，则它包含标签，则它包含的任何标签都将被忽略
* 页面标题的内容对搜索引擎优化（SEO）具有重要意义

* 通常，较长的描述性标题要比简短或一般性标题更好
    * 标题的内容是搜索引擎算法用来确定在搜索结果中列出页面顺序的因子之一
    * 同样，标题是初始的“挂钩”，您可以通过它吸引浏览搜索结果页面的读者的注意力

* 撰写好标题的准则和技巧
    * 避免使用一两个单词的标题。对于词汇表或参考样式的页面，请使用描述性短语或术语定义对
    * 搜索引擎通常显示页面标题的前 55 至 60 个字符。超出此范围的文本可能会丢失，因此请尽量不要使标题更长。如果您必须使用较长的标题，请确保重要的部分出现再前面，并且标题中可能要删除的部分中没有关键内容
    * 不要使用“关键字集合”。如果标题只是关键词列表，则算法通常会降低页面在搜索结果中的位置
    * 尝试确保您的标题在您自己的网站中尽可能唯一。标题重复（或几乎重复）可能会导致搜索结果不准确

## 常见的内容结构标签有哪些，为什么我们需要结构化 ？
##### 难度：★ ★ ★ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

（1）常见的结构标签有哪些？

* 章节


<!-- <thead>
<tr>
<th style="text-align:left"><strong>元素</strong></th>
<th style="text-align:left"><strong>描述</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">&lt;main&gt;</td>
<td style="text-align:left">定义文档中主要或重要的内容</td>
</tr>
<tr>
<td style="text-align:left">&lt;header&gt;</td>
<td style="text-align:left">定义页面或章节的头部。它包含 Logo、页面标题和导航性的目录</td>
</tr>
<tr>
<td style="text-align:left">&lt;footer&gt;</td>
<td style="text-align:left">定义页面或章节的尾部。它包含版权信息、法律信息链接和反馈建议用的地址</td>
</tr>
<tr>
<td style="text-align:left">&lt;body&gt;</td>
<td style="text-align:left">代表 HTML 文档的内容。在文档中只能有一个 &lt;body&gt; 元素</td>
</tr>
<tr>
<td style="text-align:left">&lt;section&gt;</td>
<td style="text-align:left">定义文档中的一个章节</td>
</tr>
<tr>
<td style="text-align:left">&lt;nav&gt;</td>
<td style="text-align:left">定义只包含导航链接的章节</td>
</tr>
<tr>
<td style="text-align:left">&lt;article&gt;</td>
<td style="text-align:left">定义可以独立于内容其余部分的完整独立内容块</td>
</tr>
<tr>
<td style="text-align:left">&lt;aside&gt;</td>
<td style="text-align:left">定义和页面内容关联度较低的内容，如果被删除，剩下的内容仍然合理</td>
</tr>
<tr>
<td style="text-align:left">&lt;address&gt;</td>
<td style="text-align:left">定义包含联系信息的一个章节</td>
</tr>
<tr>
<td style="text-align:left">&lt;h1&gt;-&lt;h6&gt;</td>
<td style="text-align:left">标题元素实现了六层文档标题，&lt;h1&gt; 是最大的标题，&lt;h6&gt; 是最小的标题<br>标题元素简要地描述章节的主题</td>
</tr>
</tbody> -->

* 组织


<!-- <thead>
<tr>
<th style="text-align:left"><strong>元素</strong></th>
<th style="text-align:left"><strong>描述</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">&lt;p&gt;</td>
<td style="text-align:left">定义一个段落</td>
</tr>
<tr>
<td style="text-align:left">&lt;hr&gt;</td>
<td style="text-align:left">代表章节、文章或其他长内容中的段落之间的分隔符</td>
</tr>
<tr>
<td style="text-align:left">&lt;pre&gt;</td>
<td style="text-align:left">代表其内容已经预先排版过，格式应当保留</td>
</tr>
<tr>
<td style="text-align:left">&lt;blockquote&gt;</td>
<td style="text-align:left">代表引用自其他来源的内容</td>
</tr>
<tr>
<td style="text-align:left">&lt;ol&gt;</td>
<td style="text-align:left">定义一个有序列表</td>
</tr>
<tr>
<td style="text-align:left">&lt;ul&gt;</td>
<td style="text-align:left">定义一个无序列表</td>
</tr>
<tr>
<td style="text-align:left">&lt;li&gt;</td>
<td style="text-align:left">定义列表中的一个列表项</td>
</tr>
<tr>
<td style="text-align:left">&lt;dl&gt;</td>
<td style="text-align:left">定义一个定义列表（一系列术语和其定义）</td>
</tr>
<tr>
<td style="text-align:left">&lt;dt&gt;</td>
<td style="text-align:left">定义一个由下一个 &lt;dd&gt; 定义的术语</td>
</tr>
<tr>
<td style="text-align:left">&lt;dd&gt;</td>
<td style="text-align:left">代表出现在它之前的术语的定义</td>
</tr>
<tr>
<td style="text-align:left">&lt;figure&gt;</td>
<td style="text-align:left">代表一个和文档有关的图例</td>
</tr>
<tr>
<td style="text-align:left">&lt;figcaption&gt;</td>
<td style="text-align:left">代表一个图例的说明</td>
</tr>
<tr>
<td style="text-align:left">&lt;div&gt;</td>
<td style="text-align:left">代表一个通用的容器，没有特殊含义</td>
</tr>
</tbody> -->


（2）为什么我们需要结构化？

* 便于用户在短时间内通过标题和开头找到相关内容，避免用户感到沮丧并离开
* 搜索引擎将标题视为影响排名的关键因素，没有标题，影响 SEO
* 严重视力障碍者使用听力，通过屏幕阅读器浏览网页。阅读器提供了快速访问给定文本内容的方法。通过听标题，用户能快速找到所需信息，而不需要听整个文档的大声朗读
* 便于使用 CSS 或 JavaScript 时，定位相关内容的元素

## 列表标签都有哪些 ？
##### 难度：★ ★ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆
* `<ol>` 定义一个有序列表，通常渲染为一个带编号的列表

* `<ul>` 定义一个无序列表，表示一个内可含多个元素的无序列表或项目符号列表

* `<dl>` 定义一个定义列表或描述列表元素，是一个包含术语定义以及描述的列表，通常用于展示词汇表或者元数据（键值对列表）

* `<dt>` 用于在一个定义列表中声明一个术语。该元素仅能作为 `<dl>` 子元素出现

* `<dd>` 用来指明一个描述列表（ `<dl>`）元素中一个术语的描述

    * 这个元素只能作为描述列表元素的子元素出现，并且必须跟在 `<dt>` 元素后

## 常见的标记引用标签有什么 ？
##### 难度：★ ★ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

HTML 有用于标记引用的特性，常见的标记引用标签包括：

* 块引用
    * HTML`<blockquote>` 元素（或者 HTML 块级引用元素），代表其中文字是引用内容
    * 渲染时，块引用内容会有一定缩进
    * 若引文来源于网路，则可以将原内容的出处 URL 地址设置到 `<cite>`属性上
* 行内引用
    * HTML `<q>` 元素表示一个封闭的并且是短的行内引用的文本
    * 短文本专用，不要引入换行符。长文本使用 `<blockquote>`
    * 大多数现代浏览器会为 `<q>`文本添加引号。旧浏览器可能需要使用 CSS 添加引号
    引文
    * `<cite>` 属性内容不会被浏览器现实、屏幕阅读器阅读，需使用 JavaScript 或 CSS，浏览器才会显示 `cite` 内容
    * `<cite>` 元素附上链接可以确保引用的来源在页面上是可显示的

## 如何标记缩略语 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

用 `<abbr>` 包裹一个缩略语或缩写，在 `title`中提供缩写的解释

`<acronym>` 基本上与 `<abbr>` 相同，专门用于首字母缩略词而不是缩略语

## 如何标记作者的联系方式 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

用 `<address>` 包裹 HTML 文档编写人的联系方式，支持内嵌纯文字和其它标签

## 如何现实一个化学方程式或数学公式，如何表示上标和下标 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

上标用 `<sub>` 和下标用 `<sup>` 与字母即可组合化学方程式或数学公式，例如

    (X+1)<sub>2</sub>=4 // 数学公式
    CO<sup>2</sup> // 化学方程式二氧化碳

## 如何标记计算机代码 ？
##### 难度：★ ★ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

* `<code>` 呈现一段计算机代码。通常使用浏览器的默认等宽字体显示
* `<pre>` 用来表示预定义格式文本
    * 文本通常按照原文件中的编排，以等宽字体的形式展现出来
    * 文本中的空白符（比如空白和换行符）都会显示出来
* `<var>` 表示数学表达式或变成上下文中的变量名称
    * 该行为取决于浏览器，使用当前字体的斜体形式显示
* `<kbd>` 用于表示用户输入，产生一个行内元素，通常使用浏览器 monospace 字体显示
* `<samp>` 用于标识计算机程序输出，通常使用浏览器缺省 monotype 字体显示

## 如何标记时间和日期 ？
##### 难度：★ ★ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

* `<time>` 用来表示 24 小时制时间或者公历日期，表示日期时可以包含时间和时区
* `<time>` 意在以机器可读的格式表示日期和时间
* `datetime` 属性表示此元素的时间和日期，属性值必须是有效的日期格式，并可包含时间

## 如何设置副标题 ？
##### 难度：★ ★ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

可以简单地使用 `<p>` 标签包裹副标题，或者使用标题 + `:` + 副标题的格式来声明副标题

在 HTML5 （W3C）规范中建议使用 `<hgroup>` 来表示副标题，虽然该元素已经从规范中删除，但它仍在 WHATWG 的 HTML 版本里。W3C 规范中的副标题示例代码如下：
```HTML
<!DOCTYPE HTML>
<html lang="en">
<title>Chronotype: CS Student</title>
<hgroup>
<h1> The morning </h1>
<h2> 06:00 to 12:00 </h2>
</hgroup>
<p>We sleep.</p>
<hgroup>
<h1> The afternoon </h1>
<h2> 12:00 to 18:00 </h2>
</hgroup>
<p>We study.</p>
<hgroup>
<h2>Additional Commentary</h2>
<h3>Because not all this is necessarily true</h3>
<h6>Ok it's almost certainly not true</h6>
</hgroup>
<p>Yeah we probably play, rather than study.</p>
<hgroup>
<h1> The evening </h1>
<h2> 18:00 to 00:00 </h2>
</hgroup>
<p>We play.</p>
<hgroup>
<h1> The night </h1>
<h2> 00:00 to 06:00 </h2>
</hgroup>
<p>We play some more.</p>
</html>
```
## 表象元素都有哪些 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

表象元素是指仅影响表象，没有语义的元素

`<b>` `<i>` 和 `<u>` 出现于要在文本中使用粗体、斜体和下划线但 CSS 仍然不支持的时期

表象元素不应该再被使用，因为

* 使用语义标签更有利于可读性、可访问性和 SEO
* 使用 CSS 管理样式，更利于性能优化、维护和拓展

## HTML 布局元素有哪些 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

HTML 布局元素通常是指内容分区元素，它将文档内容从逻辑上进行组织划分

使用页眉（header）、页脚（footer）、导航（nav）和标题（h1 - h6）等分区元素，来为页面内容创建明确的大纲，以便区分各个章节的内容

* `<main>` 呈现了文档的 `<body>` 或应用的主体部分，主体部分是文档的主题或主要功能
* `<article>` 元素表示文档、页面、应用或网站中的独立结构，可独立分配或复用
* `<section>` 表示在文档中的独立片段，通常包含一个标题
* `<aside>` 表示与页面主体无关，可以独立出来的部分
* `<header>` 用于展示简介，用于辅助导航或显示文章摘要，通常包含标题、Logo、搜索框、作者名称、发布时间
* `<nav>` 用于展示导航，包含到其他主要目录的链接
* `<footer>` 表示最近一个章节内容或者根节点元素的页脚。页脚通常包含该章节作者、版权数据或者与文档相关的链接
* `<address>` 表示联系信息，关联上下文，可以是地址、网址、邮箱、电话、社交账号等
* `<h1>` - `<h6>` 表示 6 个从小到大不同级别的标题， `<h1>` 级别最高， `<h6>` 级别最低

## 无语义元素有哪些，什么时候使用 ？
##### 难度：★ ☆ ☆ ☆ ☆  面试高频指数：★ ☆ ☆ ☆ ☆

无语义元素包含表象元素和 `<div>` 和 `<span>` 元素

* 表象元素包括 `<b>` `<i>` `<u>` 等仅仅影响表象但没有语义的元素，出于可读性、可访问性和 SEO 的考虑，应使用 CSS 代替它们，不再直接使用
* 将一组元素作为一个单独的实体用 CSS 修饰或 JavaScript 调用
    * `<div>` 是一个块级无语义元素，应仅用于找不到更好的块级元素时，或者不想增加特定的意义时
    * `<span>` 是一个内联无语义元素，最好只用于无法找到更好的语义元素来包含内容时，或者不想增加特定的含义时。

## 什么是可替换元素，为什么称它们为可替换元素 ？
##### 难度：★ ★ ☆ ☆ ☆  面试高频指数：★ ★ ☆ ☆ ☆

可替换元素即展现效果不由 CSS 控制，而是引用外部对象，其外观独立于 CSS，大多数情况下，CSS 仅能影响可替换元素的位置和定位方式

典型的可替换元素：

* `<iframe>`

* `<video>`

* `<embed>`

* `<img>`

* 类型为 `image` 的 `<input>` 元素
有些元素在特定情况下可作为可替换元素处理：

* `<option>`

* `<audio>`

* `<canvas>`

* `<object>`

* `<applet>`
匿名的可替换元素：

* 用 CSS 的 `content` 属性插入的对象

## 哪些标签会阻塞浏览器渲染 ？
##### 难度：★ ★ ★ ☆ ☆  面试高频指数：★ ★ ★ ☆ ☆

* `<script>` 标签会阻塞 DOM 解析
    * 内联 `<script>` 中的 JavaScript 执行完毕后，触发渲染
    * 外链 `<script>`
        * 位于 `<body>` 中，触发渲染之前的元素
        * 其它位置，不触发渲染
* `<link>` 标签不阻塞 DOM 解析，阻塞渲染和其后 JavaScript 执行
* `<img>` `<video>` `<audio>` 等可替换标签不阻塞 DOM 解析，不阻塞渲染，等渲染树生成且资源已下载后，再渲染

## 如何强制手机浏览器采用真实可视窗口宽度来加载网页 ？
##### 难度：★ ★ ☆ ☆ ☆  面试高频指数：★ ★ ★ ☆ ☆

添加 `<meta>` 标签，设置 `viewport` 属性

    <meta name=”viewport” content=”width=device-width">

* `width=device-width` 宽度是设备屏幕的宽度
* 常用于移动端自适应布局，并与以下设置项搭配使用：

* `initial-scale=1.0` 表示初始缩放比例 1.0

* `minimum-scale=1.0` 表示最小缩放比例 1.0

* `maximum-scale=1.0` 表示最大缩放比例 1.0

* `user-scalable=yes` 表示用户是否可以调整缩放比例

