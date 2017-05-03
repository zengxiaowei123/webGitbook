**\[强制\]** 页面必须使用精简形式，明确指定字符编码。指定字符编码的 meta 必须是 head 的第一个直接子元素。

解释：

见 HTML5 Charset能用吗 一文。

示例：

&lt;html&gt;

```
&lt;head&gt;

    &lt;meta charset="UTF-8"&gt;

    ......

&lt;/head&gt;

&lt;body&gt;

    ......

&lt;/body&gt;
```

&lt;/html&gt;

\[建议\] HTML 文件使用无 BOM 的 UTF-8 编码。

解释：

UTF-8 编码具有更广泛的适应性。BOM 在使用程序或工具处理文件时可能造成不必要的干扰。

