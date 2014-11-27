---
layout : post
title : "hello world"
category : Jekyll
duoshuo: true
date : 2014-10-18
tags : [Jekyll , Demo , Test , SyntaxHihglighter , pygments]
SyntaxHihglighter: true
shTheme: shThemeEclipse # shThemeDefault  shThemeDjango  shThemeEclipse  shThemeEmacs  shThemeFadeToGrey  shThemeMidnight  shThemeRDark

---

#H1

##H2

###H3

####H4

#####H5

######H6

默认字号字体

**加粗**

<!-- more -->

*斜体*
_斜体_

***加粗斜体***

内容`颜色`背景

[我是链接](http://comtu.github.com)

> 内容加边  

> 再加边  
> 再再加边  
> 再再再加边  
> 注意事项**`"内容后面有两个空格"`**  




---

	伸进

---

![图片链接](/res/img/icon.jpg)

---

* #1.H1内容

	* ##1.1H2内容
	* ###1.2H3内容
		* ####1.2.1H4内容
		* #####1.2.2H5内容
			* ######1.2.2.1H6内容
			* 01.2.2.2默认什么字号内容

		* **1.2.3加粗内容**
		* *1.2.4斜体内容*

* ***2.加粗斜体内容***
* 3.内容`颜色`背景
* 4.[我是链接](http://comtu.github.com)

1. 内容1
2. 内容2

---

下面是表格

|head1|head2|head3|head4
|---|:---|---:|:---:|
|row1text1|row1text2|row1text3|row1text4
|row2text1|row2text2|row2text3|row2text4
|row3text1|row3text2|row3text3|row3text4
|row4text1|row4text2|row4text3|row4text4

---

**[使用 pygments 高亮](http://pygments.org/)**

{% highlight c %}
/* hello world demo 代码高亮*/
#include <stdio.h>
int main(int argc, char **argv)
{
    printf("Hello, World!\n");
    return 0;
}
{% endhighlight %}


---

{% raw %}
	{% highlight c %}
	/* hello world demo 禁止解析*/
	#include <stdio.h>
	int main(int argc, char **argv)
	{
	    printf("Hello, World!\n");
	    return 0;
	}
	{% endhighlight %}
{% endraw %}

<hr id="line"/><br/>

**[用 SyntaxHihglighter 高亮](http://alexgorbatchev.com/SyntaxHighlighter/)**

<pre class="brush: js; ">
function helloSyntaxHighlighter()
{
	return "hi!";
}
</pre>

{% raw %}
	<pre class="brush: js; "><!--禁止解析-->
	function helloSyntaxHighlighter()
	{
		return "hi!";
	}
	</pre>
{% endraw %}

<pre class="brush: java; ruler: true; first-line: 0; highlight: [2, 4, 6] ; auto-links: false ; collapse: true ; gutter: false; ">
/*http://comtu.githut.io*/
class SingletonTest {
	private static class SingletonHolder {
		private static final SingletonTest INSTANCE = new SingletonTest();
	}

	private SingletonTest() {
	}

	public static final SingletonTest getInstance() {
		return SingletonHolder.INSTANCE;
	}
}

</pre>




<pre class="brush: java;  collapse: true ; first-line: 10; highlight: [11, 13, 15] " >
/**
 * 枚举_单例
 */
enum SingletonEnum {  
    INSTANCE;  
    public void whateverMethod() {  
    }  
}  
</pre>

---

**[使用 script 方式高亮](http://alexgorbatchev.com/SyntaxHighlighter/manual/installation.html)**

<script type="syntaxhighlighter" class="brush: php ; html-script: true ; collapse: true "><![CDATA[
  <html>
  <body>
      <div style="font-weight: bold"><?= str_replace("\n", "<br/>", $var) ?></div>
       
      <?
      /***********************************
       ** Multiline block comments
       **********************************/
       
      $stringWithUrl = "http://alexgorbatchev.com";
      $stringWithUrl = 'http://alexgorbatchev.com';
           
      ob_start("parseOutputBuffer");      // Start Code Buffering
      session_start();
      ?>
  </body>
  </html>
]]></script>

---

**[使用 pre 方式高亮 . 不支持 < 符号,需要进行转义为 &lt ; (但能很好的支持RSS订阅)](http://alexgorbatchev.com/SyntaxHighlighter/manual/installation.html)**

<pre class="brush: html;  collapse: true">
  &lt;html>
  &lt;body>
      &lt;div style="font-weight: bold">&lt;?= str_replace("\n", "&lt;br/>", $var) ?>&lt;/div>
       
      &lt;?
      /***********************************
       ** Multiline block comments
       **********************************/
       
      $stringWithUrl = "http://alexgorbatchev.com";
      $stringWithUrl = 'http://alexgorbatchev.com';
           
      ob_start("parseOutputBuffer");      // Start Code Buffering
      session_start();
      ?>
  &lt;/body>
  &lt;/html>
</pre>
	

[SyntaxHihglighter使用方法](http://alexgorbatchev.com/SyntaxHighlighter/manual/installation.html)

[SyntaxHihglighter参数](http://alexgorbatchev.com/SyntaxHighlighter/manual/configuration/)


<section>
<h3>最新评论</h3>
<ul class="ds-recent-comments" data-num-items="10" data-show-avatars="0" data-show-time="0" data-show-title="0" data-show-admin="0" data-excerpt-length="18"></ul>
</section>

<section style="width:250px;">
<h3>最近访客</h3>
<ul class="ds-recent-visitors" data-num-items="4" data-avatar-size="45" style="margin-top:10px;"></ul>
</section>

---
<!-- 多说评论框 start -->
    <div class="ds-thread" data-thread-key="{{ page.id }}" data-title="{{ page.title }}" data-url="{{ site.blog.url }}{{ page.url }}"></div>
<!-- 多说评论框 end -->
<!-- 多说公共JS代码 start (一个网页只需插入一次) -->
<script type="text/javascript">
var duoshuoQuery = {short_name:"sdusjy"};
    (function() {
        var ds = document.createElement('script');
        ds.type = 'text/javascript';ds.async = true;
        ds.src = (document.location.protocol == 'https:' ? 'https:' : 'http:') + '//static.duoshuo.com/embed.js';
        ds.charset = 'UTF-8';
        (document.getElementsByTagName('head')[0] 
         || document.getElementsByTagName('body')[0]).appendChild(ds);
    })();
    </script>
<!-- 多说公共JS代码 end -->

