---
layout: post
title: "Cakephp overall structure"
description: ""
category: 
tags: []
---
{% include JB/setup %}
cakephp在处理请求时，会首先通过目录下的.htaccess文件来rewrite请求,一遍？controller/action 这种请求可以转发到router解析，然后就是经典的mvc模式，相对于接触的其他php框架更为清晰，通过良好的convention极大的简化了编程，至于性能，可以通过cache等优化慢慢弥补。
![Alt cakephp](/images/cakephp-request.png)
