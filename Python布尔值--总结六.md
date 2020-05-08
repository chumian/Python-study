## 乔治·布尔

**乔治·布尔**(George Boole,1815.11.2~1864),1815年11月2日生于英格兰的林肯。19世纪最重要的数学家之一,出版了《逻辑的数学分析》 ,这是它对符号逻辑诸多贡献中的第一次。


布尔的逻辑代数理论建立在两种逻辑值“真True”、“假False”和三种逻辑关系“与AND”、“或OR”、“非NOT”。这种理论为数字电子计算机的二进制和逻辑电路的设计辅平了道路。  

冯·诺依曼奠定了现代计算机的基础，被世人尊为“计算机之父”，但在谈到他的理论与构思时，他谦虚地说，这些理论与构思的基础来自于英国数学家图灵和布尔的思想。

谷歌在2015年的网页纪念了布尔诞辰200周年,可见布尔值对人类的贡献有多大。



##布尔值
计算机的逻辑判断，只有两种结果，就是True（英文意思是“真”）和False（英文意思是“假”）。这个计算真假的过程，叫做【布尔运算】。

True和False，叫做【布尔值】。

	print(3<5) #打印出True
	print(3>5) #打印出False
	print('丽江'=='丽江') #打印出True
	print('北京'!='南京') #打印出True
print()括号内的计算其实就是【布尔运算】。终端上出现的True和False我们称为【布尔值】。
True和False就像开关一样，决定if和while循环语句是否运行。

##比较运算符
* 等于 ==  注意不是一个= 。一个 = 是赋值号，完全不相干。
* 大于  >
* 小于  <  
* 不等于  !=  
* 大于等于 >=  
* 小于等于 <=

##Python中的真假判断
在Python中 False、0、'' (空字符串)、[]（空集合）、{}（空字典） 等等为假。

其余为真，比如  2  、'学习'、True、[1]

	if '1': #条件为真
	    print('学习')
	if '': #条件为假
	    print('空空')
该段代码终端会打印出学习。

##bool()函数
	bool()函数来查看一个数据会被判断为真还是假。
	print('以下数据判断结果都是【假】：')
	print(bool(False))
	print(bool(0))
	print(bool(''))
	print(bool(None))
	
	print('以下数据判断结果都是【真】：')
	print(bool(True))
	print(bool(2))
	print(bool('szc'))

##布尔值之间的运算
**五种： and、or、not、in、not in**

**当not和and及or在一起运算时，优先级为是not>and>or**

	print(5 > 6 and 3 or 5 and 8 < 2 or not 1 > 3)   

	# 5 > 6  为 False
	# 8 <  2 为 False
	# 1 > 3  为 False
	
	# 优先级为是not>and>or
	print(False and 3 or 5 and False or not False)   
	
	# not False   为True
	# False and 3 为False
	# 5 and False 为False
	
	print(False or False or True)  
	#最终结果为True



a==1 and b==1的意思是【a=1并且b=1】，要两个条件都满足，才能判断为True。

而a==1 or b==1的意思是【a=1或者b=1】，只要两个条件满足一个，就能判断为True。

**not True就等于False，not False就等于True**

判断一个元素是否在一堆数据之中”，【not in】反之    
- --
请先阅读代码，然后直接运行

	a = 1
	b = -1
	print('以下是and运算')
	if a==1 and b==1:    # 【b实际上是-1】
	    print('True')
	else:
	    print('False')
	#打印出False

	print('以下是or运算')
	if a==1 or b==1:  # 【b实际上是-1】
	    print('True')
	else:
	    print('False')
	#打印出True
-  --	
直接运行代码即可

	list1 = [1,2,3,4,5]
	a = 1
	# 做一次布尔运算，判断“a是否在列表list之中”
	print(bool(a in list1))
	print(bool(a not in list1))
	

	list2 = ['apple','milk','c']
	print(bool(a not in list2))
	print(bool('a' in list2))
	print(bool('c' in list2))

\>>>  
True  
False  
True  
False  
True  
