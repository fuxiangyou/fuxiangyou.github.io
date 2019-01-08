---
title: Python3学习(六) -- IO操作
date: 2018-12-05 13:38:05
tags:
---
## 文件
### open()
  - 语法：

	`open(file, mode='r', buffering=-1, encoding=None, errors=None, newline=None, closefd=True, opener=None)`
	
  - 参数说明:
    - file: 必须，文件的相对/绝对路径
    - buffering: 可选，设置缓冲
    - encoding: 可选，编码格式
    - errors: 可选，报错级别
    - newline: 区分换行符
    - closefd: 传入的file参数类型
    - opener: 
    - mode: 可选, 文件打开模式
    
	| 打开模式 | 执行操作 |
	| :------:| :------: |
	| 't' | 以文本模式打开文件(默认) |
	| 'x' | 写模式，使用此模式时，如果文件已经存在则会抛异常 |
	| 'b' | 以二进制模式打开文件 |
	| '+' | 可读写模式(可与其他模式一块使用，例如: r+) |
	| 'U' | 通用换行符支持 |
	| 'r' | 以只读方式打开文件,指针在文件开头(默认) |
	| 'w' | 以只写方式打开文件，指针从头开始，如果文件存在则会覆盖原先内容，覆盖操作 |
	| 'a' | 以只写方式打开文件，如果文件存在则指针直接跳到文本末尾，追加操作 |
	
	
### 文件对象 file

####文件对象常用函数:

| 文件对象方法 | 执行操作 |
| :------:| :------: |
| file.read(size) | 从文件中读取size个字符，size为负或者未给定时，读取剩余所有字符并作为string返回 |
| file.readline() | 读取一行作为字符串返回 |
| file.write(str) | 将字符串str写入 |
| file.writelines(seq) | 将字符串序列seq写入 |
| file.seek(offset,from) | 在文件中移动文件指针，从from(0:起始位置;1:当前位置;2:末尾位置)处偏移offset个字节 |
| file.tell() | 返回当前指针在文件中的位置 |
| file.flush() | 刷新文件内部缓存，直接把内部缓冲区的数据立刻写入文件，而不是被动等待输出缓冲区写入 |
| file.next() | 返回文件下一行 |

<font color="red">未完待续。。。</font>