##RegExp类型
<pre>var expression = /patten/flags</pre>
>(patten):模式部分可以是任何简单或复杂的正则表达式，可以包括字符类，限定符分组，向前查找或反向引用。<br />
>(flags):标志，用以表达正则表达式的行为<br />
><ul>
	<li>g:表示全局模式，即模式将被应用与所有字符串，而非在发现第一	个匹配项时停止。
	<li>i:表示不区分大小写(case-insensitive)模式，即在确定匹配项	时忽略模式于字符串的大小写。
	<li>m:表示多行(multiline)模式，即在到达一行末尾时还会继续查找	下一行中是否存在与模式匹配的项
></ul>

例：
<pre>var pattern1=/at/g;  v   //匹配字符串中所有“at”实例
var pattern2=/[bc]at/g;  //匹配字符串中所有“cat”和“bat”实例
</pre>
<li>模式中所有元字符必须转义<br>
例：
<pre>
var pattern1 = /\[bc\]at/i; //匹配字符串中第一个'[bc]at'实例
var pattern2 = /\.at/gi;    //匹配字符串中所有.at，不区分大小写
</pre></li>
<li>另一种构建正则表达式的方式 
<pre>var pattern = new RegExp("pattern","flags")</pre>
传递给RegExp函数的两个参数要都是字符串，在某种情况下要进行双重转义
<table>
<tr><td>字面量模式</td><td>等价的字符串</td></tr>
<tr><td>/\[bc\]at/</td><td>"\\[bc\\]at"</td></tr>
<tr><td>/\.at/</td><td>"\\.at"</td></tr>
<tr><td>/name\/age/</td><td>"name\\/age"</td></tr>
<tr><td>/\d.\d{1.2}/</td><td>"\\d.\\d{1.2}"</td></tr>
<tr><td>/\w\\hello\\123/</td><td>"\\w\\\\hello\\\\123"</td></tr>
<tr><td>......</td><td>......</td></tr>
</table>
</li>
<li>使用正则表达式字面量和使用RegExp构造函数创建的正则表达式不一样
>ECMAScript3中，使用正则表达式字面量始终会共享一个RegExp实例，而使用RegExp函数创建的每一个新RegExp实例都是新实例。
>ECMAScript5明确规定，使用正则表达式字面量必须向直接调用RegExp构造函数一样，创建新的实例。
</li>
###RegExp实例属性
<li>global:布尔值，表示是否设置了g标签。</li>
<li>ignoreCase:布尔值，表示是否设置了i标签。</li>
<li>multiline:</li>
