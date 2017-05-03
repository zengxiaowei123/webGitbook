**\[强制\]** 页面必须包含 title 标签声明标题。

**\[强制\]** title 必须作为 head 的直接子元素，并紧随 charset 声明之后。

解释：

title 中如果包含 ascii 之外的字符，浏览器需要知道字符编码类型才能进行解码，否则可能导致乱码。

示例：

&lt;head&gt;

```
&lt;meta charset="UTF-8"&gt;

&lt;title&gt;页面标题&lt;/title&gt;
```

&lt;/head&gt;

