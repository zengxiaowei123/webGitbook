\[建议\] 负责主要功能的按钮在 DOM 中的顺序应靠前。

解释：

负责主要功能的按钮应相对靠前，以提高可访问性。如果在 CSS 中指定了 float: right 则可能导致视觉上主按钮在前，而 DOM 中主按钮靠后的情况。

示例：

&lt;!-- good --&gt;

&lt;style&gt;

.buttons .button-group {

    float: right;

}

&lt;/style&gt;



&lt;div class="buttons"&gt;

    &lt;div class="button-group"&gt;

        &lt;button type="submit"&gt;提交&lt;/button&gt;

        &lt;button type="button"&gt;取消&lt;/button&gt;

    &lt;/div&gt;

&lt;/div&gt;



&lt;!-- bad --&gt;

&lt;style&gt;

.buttons button {

    float: right;

}

&lt;/style&gt;



&lt;div class="buttons"&gt;

    &lt;button type="button"&gt;取消&lt;/button&gt;

    &lt;button type="submit"&gt;提交&lt;/button&gt;

&lt;/div&gt;

\[建议\] 当使用 JavaScript 进行表单提交时，如果条件允许，应使原生提交功能正常工作。

解释：

当浏览器 JS 运行错误或关闭 JS 时，提交功能将无法工作。如果正确指定了 form 元素的 action 属性和表单控件的 name 属性时，提交仍可继续进行。

示例：

&lt;form action="/login" method="post"&gt;

    &lt;p&gt;&lt;input name="username" type="text" placeholder="用户名"&gt;&lt;/p&gt;

    &lt;p&gt;&lt;input name="password" type="password" placeholder="密码"&gt;&lt;/p&gt;

&lt;/form&gt;

\[建议\] 在针对移动设备开发的页面时，根据内容类型指定输入框的 type 属性。

解释：

根据内容类型指定输入框类型，能获得能友好的输入体验。

示例：

&lt;input type="date"&gt;



