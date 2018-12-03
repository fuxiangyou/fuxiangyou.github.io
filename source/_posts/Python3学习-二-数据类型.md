---
title: Python3学习(二) -- 数据类型
date: 2018-11-30 10:50:21
tags:
---
## 数据类型['Number','String','List','Tupe','Set','Dictionary']

  - string、list、tuple都属于sequence(序列)

### Number(数字类型)
#### int(整形)
  - 所有整数类型，不再区分长整型

#### float(浮点型)
  - 所有小数类型
  - E记法：用于表示特别大和特别小的数

		 >>> a = 0.00000000000000000000011  
		 >>> a
		 1.1e-22 //类似于1.1 乘以 10的-22次方

#### bool(布尔类型)
   -	true 相当于1
   -   false 相当于0
   -   在python3中，布尔类型本质还是数字，可以做加减运算

#### complex(复数)
  - 复数由实数部分和虚数部分构成，可以用a+bj或者complex(a,b)表示，例如2E+6J,a和b都是float类型

### String(字符串)

  - 截取语法 变量[头下表:尾下标:取值方式]：索引从0开始，-1表示尾部最后一位（\-:表示倒数;1:表示第一位），取值方式：符号\+数字N，默认为1(\-：表示倒序；数字N表示每N个字符中取第一个)

  		>>> str = "嘿！兄弟，下午好!"
		>>> print(str[0:2])
		嘿！
		>>> print(str[2:])
		兄弟，下午好!
		>>> print(str[2::1])
		兄弟，下午好!
		>>> print(str[::-1])
		!好午下，弟兄！嘿	
		>>> print(str[::-2])
		!午，兄嘿
		>>> print(str[::2])
		嘿兄，午!
		>>> print(str[2::-1])
		兄！嘿	
  - +：字符串连接符
  - *：表示复制当前字符串，后面加数字表示复制次数

  		>>> str = "付先生 " * 3
		>>> str
		'付先生 付先生 付先生 '

#### 输出原始字符串（不用再进行转译）:r 字符串

	>>> string = r'C:\mac'
	>>> string
	'C:\\mac'
	>>> print(string)
	C:\mac

#### 长字符串：解决文章类的带格式的长字符串翻译问题

	>>> string = """哈喽：
	...             亲爱的朋友。"""
	>>> string
	'哈喽：\n            亲爱的朋友。'
	>>> print(string)
	哈喽：
            亲爱的朋友。

### List(数组)

  - 格式：['','']&nbsp;&nbsp;\(List写在方括号之间，元素用逗号隔开)
  - 元素可以重复 支持各种数据类型混用
  - 切片(截取)，索引方式和String一致

	  	>>> list = [1,2,3,4,5,6]
		>>> list2 = [7]
		>>> print(list)
		[1, 2, 3, 4, 5, 6]
		>>> print(list[1:3])
		[2, 3]
		>>> print(list[3:])
		[4, 5, 6]
		>>> print(list[::-1])
		[6, 5, 4, 3, 2, 1]
		>>> print(list[::-1]*2)
		[6, 5, 4, 3, 2, 1, 6, 5, 4, 3, 2, 1]
		>>> print(list[::-1]+list2)
		[6, 5, 4, 3, 2, 1, 7]

### Tuple(元组)
  - 切片(截取),索引方式和String一致
  - 元素不可修改，但可以包含可变元素
  - 格式：	(,)&nbsp;&nbsp;\(List写在小括号之间，元素用逗号隔开)
  - <font color="red">赋值一个元素时也需要逗号: tup=(10,)</font>

		>>> tuple = ('a','b','c','d','e','f','g')
		>>> tuple2 = (1,)
		>>> print(tuple)
		('a', 'b', 'c', 'd', 'e', 'f', 'g')
		>>> print(tuple[0])
		a
		>>> print(tuple[1:2])
		('b',)
		>>> print(tuple[1:3])
		('b', 'c')
		>>> print(tuple[3:])
		('d', 'e', 'f', 'g')
		>>> print(tuple[::-1])
		('g', 'f', 'e', 'd', 'c', 'b', 'a')
		>>> print(tuple[::-1]*2)
		('g', 'f', 'e', 'd', 'c', 'b', 'a', 'g', 'f', 'e', 'd', 'c', 'b', 'a')
		>>> print(tuple+tuple2)
		('a', 'b', 'c', 'd', 'e', 'f', 'g', 1)

### Set(集合)
  - 格式: {,}&nbsp;&nbsp;\(Set写在小括号之间，元素用逗号隔开)

### 类型转换
  - int() 将字符串或者浮点数转换成一个整数  <font color="red">浮点数转整数时只保留整数，不会四舍五入</font>
  - float() 将字符串或者整数转换成浮点数
  - str() 将其他数据类型转换成字符串
  - <font color="red">type() 查看变量类型</font>
  - <font color="red">isinstance() 判断变量类型</font>

