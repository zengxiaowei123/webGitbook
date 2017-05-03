\[强制\] 保证 favicon 可访问。

解释：

在未指定 favicon 时，大多数浏览器会请求 Web Server 根目录下的 favicon.ico 。为了保证favicon可访问，避免404，必须遵循以下两种方法之一：

1.	在 Web Server 根目录放置 favicon.ico 文件。

2.	使用 link 指定 favicon。

示例：

&lt;link rel="shortcut icon" href="path/to/favicon.ico"&gt;



