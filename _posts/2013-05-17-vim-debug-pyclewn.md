---
layout: post
title: "debug with vim and gdb: Pyclewn"
description: ""
category: 
tags: []
---
{% include JB/setup %}
[pyclewn](http://pyclewn.sourceforge.net/)是vimgdb类似的工具，不同是不用想vimgdb一样给vim打补丁，它是基于python的工具，可以让vim变成变成gdb的调试前端。

安装过程:

	sudo su
	tar xzf pyclewn-1.10.py3.tar.gz
	cd pyclewn-1.10.py3
	export EDITOR=PATH TO VIM
	python setup.py install --force

也可以通过 --home=PATH 来指定安装位置以及export vimdir=.vim将vim相关的插件等文件本地安装。

使用：

	vim test.cpp
	:Pyclewn

这样就开启了Pyclewn，然后Cxx的命令相当于映射到了gdb里所以

	:Cfile test
	
这样相当与用file加载了文件(假设已经make),然后Cmapkeys可以**加载**所有快捷键比如Shift R运行程序，Ctrl N下一步

	:Cbreak 3
	:Cdbgvar i 

设置一个断点,监视变量i
具体可以参考
	
 	:help Pyclewn

![alt screen shot](/images/pyclewn-vim.png)
