\[强制\] 有文本标题的控件必须使用 label 标签将其与其标题相关联。

解释：

有两种方式：

1.	将控件置于 label 内。

2.	label 的 for 属性指向控件的 id。

推荐使用第一种，减少不必要的 id。如果 DOM 结构不允许直接嵌套，则应使用第二种。

示例：

&lt;label&gt;&lt;input type="checkbox" name="confirm" value="on"&gt; 我已确认上述条款&lt;/label&gt;



&lt;label for="username"&gt;用户名：&lt;/label&gt; &lt;input type="textbox" name="username" id="username"&gt;



