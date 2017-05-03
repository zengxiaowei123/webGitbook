\[建议\] 模板代码的缩进优先保证 HTML 代码的缩进规则。

示例：

&lt;!-- good --&gt;

{if $display == true}

&lt;div&gt;

    &lt;ul&gt;

    {foreach $item\_list as $item}

        &lt;li&gt;{$item.name}&lt;li&gt;

    {/foreach}

    &lt;/ul&gt;

&lt;/div&gt;

{/if}



&lt;!-- bad --&gt;

{if $display == true}

    &lt;div&gt;

        &lt;ul&gt;

    {foreach $item\_list as $item}

        &lt;li&gt;{$item.name}&lt;li&gt;

    {/foreach}

        &lt;/ul&gt;

    &lt;/div&gt;

{/if}

\[建议\] 模板代码应以保证 HTML 单个标签语法的正确性为基本原则。

示例：

&lt;!-- good --&gt;

&lt;li class="{if $item.type\_id == $current\_type}focus{/if}"&gt;{ $item.type\_name }&lt;/li&gt;



&lt;!-- bad --&gt;

&lt;li {if $item.type\_id == $current\_type} class="focus"{/if}&gt;{ $item.type\_name }&lt;/li&gt;

\[建议\] 在循环处理模板数据构造表格时，若要求每行输出固定的个数，建议先将数据分组，之后再循环输出。

示例：

&lt;!-- good --&gt;

&lt;table&gt;

    {foreach $item\_list as $item\_group}

    &lt;tr&gt;

        {foreach $item\_group as $item}

        &lt;td&gt;{ $item.name }&lt;/td&gt;

        {/foreach}

    &lt;tr&gt;

    {/foreach}

&lt;/table&gt;



&lt;!-- bad --&gt;

&lt;table&gt;

&lt;tr&gt;

    {foreach $item\_list as $item}

    &lt;td&gt;{ $item.name }&lt;/td&gt;

        {if $item@iteration is div by 5}

    &lt;/tr&gt;

    &lt;tr&gt;

        {/if}

    {/foreach}

&lt;/tr&gt;

&lt;/table&gt;



