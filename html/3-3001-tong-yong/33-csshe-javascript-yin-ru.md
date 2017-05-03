\[强制\] 引入 CSS 时必须指明 rel="stylesheet"。

示例：

&lt;link rel="stylesheet" src="page.css"&gt;

\[建议\] 引入 CSS 和 JavaScript 时无须指明 type 属性。

解释：

text/css 和 text/javascript 是 type 的默认值。

\[建议\] 展现定义放置于外部 CSS 中，行为定义放置于外部 JavaScript 中。

解释：

结构-样式-行为的代码分离，对于提高代码的可阅读性和维护性都有好处。

\[建议\] 在 head 中引入页面需要的所有 CSS 资源。

解释：

在页面渲染的过程中，新的CSS可能导致元素的样式重新计算和绘制，页面闪烁。

\[建议\] JavaScript 应当放在页面末尾，或采用异步加载。

解释：

将 script 放在页面中间将阻断页面的渲染。出于性能方面的考虑，如非必要，请遵守此条建议。

示例：

&lt;body&gt;

    &lt;!-- a lot of elements --&gt;

    &lt;script src="init-behavior.js"&gt;&lt;/script&gt;

&lt;/body&gt;

\[建议\] 移动环境或只针对现代浏览器设计的 Web 应用，如果引用外部资源的 URL 协议部分与页面相同，建议省略协议前缀。

解释：

使用 protocol-relative URL 引入 CSS，在 IE7/8 下，会发两次请求。是否使用 protocol-relative URL 应充分考虑页面针对的环境。

示例：

&lt;script src="//s1.bdstatic.com/cache/static/jquery-1.10.2.min\_f2fb5194.js"&gt;&lt;/script&gt;



