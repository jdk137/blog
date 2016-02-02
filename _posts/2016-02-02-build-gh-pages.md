---
layout: default
title: gh-pages 首次搭建遇到的坑
---

{{ page.title }}
================

主要参考了 阮一峰的博客 [搭建一个免费的，无限流量的Blog----github Pages和Jekyll入门](http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html)

因为这个博客是几年前的了，有些地方还是有走不过去的情况。

其中有 

1. gh pages DNS ip地址已变更。请参考 [这个git文档](https://help.github.com/articles/tips-for-configuring-an-a-record-with-your-dns-provider/)

2. 复制html内容时可能的问题。这在原博客评论中有解决 

  请确认yaml头是否书写正确。三根短划线前面，是不能有空格的！
  
  如果你用windows，必须确认保存文件的时候不带BOM。
  
3. 绑定域名后将_config.yml文件中的baseurl改成根目录"/"。这个是不行的，首页单篇文章的链接无法解析了。最后修改了index.html中的'{{ site.baseurl }}' 为 '.'

就是这些了。可以跑起来的，但要美观实用，还有许多东西要解决，特别是要学习下Jekyll以及这个[示例库](https://github.com/mojombo/tpw)。最重要的收获还是学到了为项目快速搭建文档说明页的方法。

感谢阮一峰的文章。欢迎大家关注 [happyjdk.com](happyjdk.com)! :)
