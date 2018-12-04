---
title: Python3学习(四) -- 流程控制语句
date: 2018-12-03 17:12:22
tags:
---

## 条件控制语句: if else
  - 语法

		if 条件1：
			条件1为true执行的操作
		elif 条件2：
			条件2为true执行的操作
		else:
			其他条件为true执行的操作	
				
## 循环语句
### while
  - 语法

		while 条件:
			循环体
		else:
			不满足条件执行语句
  		
例：

	>>> a = 0
	>>> while a < 3:
	...     print (a)
	...     a += 1
	... else:
	...     print ("a = ",a)
	...
	0
	1
	2
	a =  3
	
### for
  - 语法

		for 自定义接收变量 in 序列类型：
			循环体
		else:
			迭代完执行语句（<font color = "red">当最后一个迭代循环体有break时不执行</font>）
			
例句1：

	>>> for b in range(1,5):
	...     print ("b = ",b)
	... else:
	...     print('我是数字:',b)
	...
	b =  1
	b =  2
	b =  3
	b =  4
	我是数字: 4
	
例句2:

	>>> for b in range(1,5):
	...     print ("b = ",b)
	...     break
	... else:
	...     print ('我是数字:',b)
	...
	b =  1

例句3:

	>>> for b in range(1, 5):
	...     print ("b = ", b)
	...     continue
	... else:
	...     print ("我是数字:", b)
	...
	b =  1
	b =  2
	b =  3
	b =  4
	我是数字: 4
	
<font color = "red">扩展：break：跳出循环体；continue：结束本次循环开始下轮循环</font>



<font color="red">未完待续。。。</font>