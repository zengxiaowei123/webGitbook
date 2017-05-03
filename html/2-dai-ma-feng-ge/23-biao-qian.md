**\[强制\]** 标签名必须使用小写字母。

示例：

&lt;!-- good --&gt;

&lt;p&gt;Hello StyleGuide!&lt;/p&gt;

&lt;!-- bad --&gt;

&lt;P&gt;Hello StyleGuide!&lt;/P&gt;

**\[强制\]** 对于无需自闭合的标签，不允许自闭合。

解释：

常见无需自闭合标签有input、br、img、hr等。

示例：

&lt;!-- good --&gt;

&lt;input type="text" name="title"&gt;

&lt;!-- bad --&gt;

&lt;input type="text" name="title" /&gt;

**\[强制\]** 对 HTML5 中规定允许省略的闭合标签，不允许省略闭合标签。

解释：

对代码体积要求非常严苛的场景，可以例外。比如：第三方页面使用的投放系统。

示例：

&lt;!-- good --&gt;

&lt;ul&gt;

```
&lt;li&gt;first&lt;/li&gt;

&lt;li&gt;second&lt;/li&gt;
```

&lt;/ul&gt;

&lt;!-- bad --&gt;

&lt;ul&gt;

```
&lt;li&gt;first

&lt;li&gt;second
```

&lt;/ul&gt;

**\[强制\]** 标签使用必须符合标签嵌套规则。

解释：

比如 div 不得置于 p 中，tbody 必须置于 table 中。

详细的标签嵌套规则参见HTML DTD中的 Elements 定义部分。

\[建议\] HTML 标签的使用应该遵循标签的语义。

解释：

下面是常见标签语义

•    p - 段落

•    h1,h2,h3,h4,h5,h6 - 层级标题

•    strong,em - 强调

•    ins - 插入

•    del - 删除

•    abbr - 缩写

•    code - 代码标识

•    cite - 引述来源作品的标题

•    q - 引用

•    blockquote - 一段或长篇引用

•    ul - 无序列表

•    ol - 有序列表

•    dl,dt,dd - 定义列表

示例：

&lt;!-- good --&gt;

&lt;p&gt;Esprima serves as an important &lt;strong&gt;building block&lt;/strong&gt; for some JavaScript language tools.&lt;/p&gt;

&lt;!-- bad --&gt;

&lt;div&gt;Esprima serves as an important &lt;span class="strong"&gt;building block&lt;/span&gt; for some JavaScript language tools.&lt;/div&gt;

\[建议\] 在 CSS 可以实现相同需求的情况下不得使用表格进行布局。

解释：

在兼容性允许的情况下应尽量保持语义正确性。对网格对齐和拉伸性有严格要求的场景允许例外，如多列复杂表单。

\[建议\] 标签的使用应尽量简洁，减少不必要的标签。

示例：

&lt;!-- good --&gt;

&lt;img class="avatar" src="image.png"&gt;

&lt;!-- bad --&gt;

&lt;span class="avatar"&gt;

```
&lt;img src="image.png"&gt;
```

&lt;/span&gt;

