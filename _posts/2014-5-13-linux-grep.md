---
layout: post
title: "linux命令--grep"
description: "linux"
category:
tags: [linux]
---
{% include JB/setup %}

0. grep以行为单位  
1. `$ dpkg -l | grep -i 'php'`  

	`dpkg -l`是列出系统上安装的deb包，-i是忽略大小写。  
2. `$ grep -v "#" /etc/apache2/sites-available/default-ssl | tr -s '\n'`  
	
	输出`default-sll`文件中没有#的所有行,`tr -s '\n'`表示删除重复的`\n`  
3. `$ find . -name "*.mp3" | grep -i JayZ | grep -vi "remix"`    
	
	找到当前目录下所有mp3文件中，名字含有jayz不含remix  
4. `$ ifconfig | grep -A 4 'eth0'`  
	
	显示含有eth0的一行和它之后的4行，此处 A=after，另外类似 B=before  
5. `$ ifconfig | grep -c ‘inet6’`  
	
	计算含有‘inet6’的行数，类似于 `$ ifconfig | grep 'inet6' | wc -l`   
6. `$ grep -n 'print'  hello.py`   
	
	显示含有print的行内容，并显示行号
