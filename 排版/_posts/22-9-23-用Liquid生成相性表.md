{{"羊牛双蟹狮处秤蝎射摩瓶鱼"|split:""|join:"|"}}
{%-assign a="热冷"|split:""%}
{%for i in(0..11)%}{%assign b=i|modulo:2%}{{a[b]}}|{%endfor%}
{%-assign a="干湿"|split:""%}
{%for i in(0..11)%}{%assign b=i|divided_by:2|modulo:2%}{{a[b]}}|{%endfor%}
{%-assign a="基固变"|split:""%}
{%for i in(0..11)%}{%assign b=i|modulo:3%}{{a[b]}}|{%endfor%}

```Liquid
{%raw%}{{"羊牛双蟹狮处秤蝎射摩瓶鱼"|split:""|join:"|"}}
{%-assign a="热冷"|split:""%}
{%for i in(0..11)%}{%assign b=i|modulo:2%}{{a[b]}}|{%endfor%}
{%-assign a="干湿"|split:""%}
{%for i in(0..11)%}{%assign b=i|divided_by:2|modulo:2%}{{a[b]}}|{%endfor%}
{%-assign a="基固变"|split:""%}
{%for i in(0..11)%}{%assign b=i|modulo:3%}{{a[b]}}|{%endfor%}{%endraw%}
```

作为学习Liquid的一次尝试，
Liquid本身设计是模板语言，
普通编程的语法和格式都不支持，
生成复杂数据，也能做到，但完全不合适。

以这段代码来说，
一是常用的除、模运算符就不支持，要用啰嗦的语法，
二是传参都必须先显性声明变量，也是非常啰嗦。

只用Liquid处理模板，
不用来处理内容，或者说模板之外的任何内容。
