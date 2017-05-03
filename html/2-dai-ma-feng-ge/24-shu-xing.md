\[强制\] 属性名必须使用小写字母。

示例：

&lt;!-- good --&gt;

&lt;table cellspacing="0"&gt;...&lt;/table&gt;

&lt;!-- bad --&gt;

&lt;table cellSpacing="0"&gt;...&lt;/table&gt;

\[强制\] 属性值必须用双引号包围。

解释：

不允许使用单引号，不允许不使用引号。

示例：

&lt;!-- good --&gt;

&lt;script src="esl.js"&gt;&lt;/script&gt;

&lt;!-- bad --&gt;

&lt;script src='esl.js'&gt;&lt;/script&gt;

&lt;script src=esl.js&gt;&lt;/script&gt;

\[建议\] 布尔类型的属性，建议不添加属性值。

示例：

&lt;input type="text" disabled&gt;

&lt;input type="checkbox" value="1" checked&gt;

\[建议\] 自定义属性建议以 xxx- 为前缀，推荐使用 data-。

解释：

使用前缀有助于区分自定义属性和标准定义的属性。

示例：

&lt;ol data-ui-type="Select"&gt;&lt;/ol&gt;

