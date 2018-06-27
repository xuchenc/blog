# 前端工程化简史


##  前端工程师的技能栈

1.**硬技能——HTML/CSS/JavaScript**

这三项俗称“前端工程师的三把刷子”，是前端工程师必备三大项。HTML和CSS作为标记类语言，只有在浏览器环境或者类浏览器环境下才会被识别解析；而JavaScript不同，其本质上是一门编程语言。同其他编程语言一样，对于JavaScript，掌握其语法和特性是最基本的。但上面这些只是应用能力，最终考量的仍然是计算机体系的理论知识。所以，数据结构、算法、软件工程等基础知识对于前端工程师同样重要，这些知识能够决定一个前端工程师的上限。

2.**软技能——用户体验**

前端工程师的产出是直接面向用户的，良好的用户体验是一个web产品的基本要素。<em>这里的用户体验并非指的是交互方案和视觉设计，当然这些也是用户体验的一部分。</em>此处我们讨论包括以下几点。

**a.**保证内容的快速展现，减少用户等待时间。

**b.**保证操作的流畅性。

**c.**如果是移动设备，应尽量减少设备的耗电量。

3.**扩展技能——Node.js**

这里的Node.js并非指的Node.js本身，而是以Node.js为代表的Web服务端知识。前端工程师掌握Web客户端的相关知识是基本要求，欠缺的是对Web服务器端的了解。

前端工程师是承载用户层所有功能的资源产出者，不仅是客户端最终呈现给用户的HTML/CSS/JavaScript等资源成品，而且还包括这些资源从零开始到最终产出的生产流水线所涵盖的所有环节。

## 前端的两次新生

1.**第一次新生：AJAX**

AJAX技术起步于微软的Outlook的XMLHTTP组件，后来其他浏览器厂商实现了一个同样的JavaScript对象——XMLHttpRequest。

AJAX技术可以实现异步请求和局部刷新，彻底改变了传统Web站点的交互模式。

2.**第二次新生：Node.js**

2009年第一版的Node.js的发布是值得铭记的里程碑。<em>Node.js的作者设计Node.js的灵感来自一个上传进度条，浏览器为了能够获取上传文件的进度而不得不频繁地向服务器发起查询请求。与这种方式相比，如果服务器能够在文件上传完毕后，主动推送一条消息给浏览器的话，会节省很多的浏览器和网络资源消耗。这种理念便是Node.js实现异步操作的核心**Event Loop（事件驱动）的雏形。**</em>JavaScript终于进入了服务器端开发领域，更重要的意义是丰富了JavaScript的生态。

与PHP不同的是，Node.js可以直接提供网络服务，不需要借助Apache、Nginx等专业的服务器软件。

## 大前端

之所以称为“大前端”而不是“全栈工程师”是因为大前端通常不接触数据库操作。大前端负责的并不是真正的Web服务层，而是中间层。中间层的作用主要解决的就是HTML的渲染，这也是为了实现前后端分离而探索出的一个模式。

## 前端工程化的进化历程

1.**混沌形态**

我们不妨将这种“前端写demo，后端写逻辑、套模板”的开发模式称为“混沌形态”。这种形态的时代背景是Web产品的逻辑和交互普遍比较简单，前端工程师这一专业岗位刚刚兴起，但是负责的工作仅仅是样式以及部分动画逻辑。前端工程师与后端工程师之间的协作是串行的。

2.**前后端分析形态**

前后端分离后，前端逻辑、样式和HTML全部交由前端工程师开发。这是催生前端工程化萌芽的关键一步，但是日渐庞大的前端面临着许多问题：

 开发层面

- ES规范与浏览器兼容性不一致。

- CSS的弱编程能力。

-  资源定位。

-  图片压缩/base64内嵌/CSS Sprites。

-  模块依赖分析和压缩打包。

 协作层面

-  JavaScript部分逻辑依赖接口API（mock数据）。

 部署层面

-  部分资源需要借助后端工程师部署。


**工程化方案架构**

——webpack（前端工具有很多，这里只讨论我比较熟悉的webpack）

**构建功能规划**

构建系统是整个工程化方案中最重要也是最复杂的功能，主要解决的是前端开发层面的问题。书中介绍的工程化方案Boi将内置以下功能。

- ES规范的转译。

- CSS预编译器支持。

- PostCSS处理hack后缀。

- 自动创建CSS Sprites图。

- 图片压缩。

- 小体积图片base64内嵌。

- JavaScript模块化规范支持。

除以上功能以外，Boi针对不同的缓存策略可以支持增量更新（chunkhash）与覆盖更新构建。

## 总结

Web技术的发展催生用户对Web产品产生更多、更复杂的需求，进而推动前端工程师开发任务的细化和加重。功能、逻辑、资源不断复杂化、多样化进一步促进了前端工程化的诞生。得益于 Node.js、前端工具生态的不断进步和扩大，令前端工程化方案的实施有了必要的环境条件。

前端工程化的进化历程伴随着前后端工程师分工的改变而改变。前后端分离是Web 产品开发分化的必然趋势，前端工程化的核心目标之一便是建立合理的前后端分离工作环境，提高团队整体的工作效率。本地工具链形态的工程化通过Mock服务实现了前后端并行开发，统一的工具栈加强了规范意识和约束，减少了业务开发人员的学习成本。云管理平台形态的工程化（同意本地开发环境）进一步淡化了差异性并加深了规范。

读书笔记《[前端工程化：体系设计与实践][1]》


  [1]: http://item.jd.com/12285480.html