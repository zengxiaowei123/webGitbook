\[强制\] class 必须单词全字母小写，单词间以 - 分隔。

\[强制\] class 必须代表相应模块或部件的内容或功能，不得以样式信息进行命名。

示例：

&lt;!-- good --&gt;

&lt;div class="sidebar"&gt;&lt;/div&gt;

&lt;!-- bad --&gt;

&lt;div class="left"&gt;&lt;/div&gt;

\[强制\] 元素 id 必须保证页面唯一。

解释：

同一个页面中，不同的元素包含相同的 id，不符合 id 的属性含义。并且使用 document.getElementById 时可能导致难以追查的问题。

\[建议\] id 建议单词全字母小写，单词间以 - 分隔。同项目必须保持风格一致。

\[建议\] id、class 命名，在避免冲突并描述清楚的前提下尽可能短。

示例：

&lt;!-- good --&gt;

&lt;div id="nav"&gt;&lt;/div&gt;

&lt;!-- bad --&gt;

&lt;div id="navigation"&gt;&lt;/div&gt;

&lt;!-- good --&gt;

&lt;p class="comment"&gt;&lt;/p&gt;

&lt;!-- bad --&gt;

&lt;p class="com"&gt;&lt;/p&gt;

&lt;!-- good --&gt;

&lt;span class="author"&gt;&lt;/span&gt;

&lt;!-- bad --&gt;

&lt;span class="red"&gt;&lt;/span&gt;

\[强制\] 禁止为了 hook 脚本，创建无样式信息的 class。

解释：

不允许 class 只用于让 JavaScript 选择某些元素，class 应该具有明确的语义和样式。否则容易导致 css class 泛滥。

使用 id、属性选择作为 hook 是更好的方式。

\[强制\] 同一页面，应避免使用相同的 name 与 id。

解释：

IE 浏览器会混淆元素的 id 和 name 属性， document.getElementById 可能获得不期望的元素。所以在对元素的 id 与 name 属性的命名需要非常小心。

一个比较好的实践是，为 id 和 name 使用不同的命名法。

示例：

&lt;input name="foo"&gt;

&lt;div id="foo"&gt;&lt;/div&gt;

&lt;script&gt;

// IE6 将显示 INPUT

alert\(document.getElementById\('foo'\).tagName\);

&lt;/script&gt;

