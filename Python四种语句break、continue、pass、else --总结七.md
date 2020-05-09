##break语句

这是break的含义，在python循环结构中使用，也是这么个意思，打破循环，也就是结束循环，开始下面的内容。

我们看看它的用法，请注意里面的缩进：
### break语句搭配for循环
	for...in...:
	    ...
	    if ...:
	        break

### break语句搭配while循环
	while...(条件):
	    ...
	    if ...:
	        break
-  ----
我们看一个《明日歌》的for循环的实例先:  
请运行代码体验效果

	for i in range(5):
	    print('明日复明日')
	    if i==3:  # 当i等于3的时候触发
	        break # 结束循环


## continue语句
continue是继续的意思，break是打断、打破的意思。

因此，虽然同用于循环结构，但是continue却是返回到循环开头，并根据测试结果决定是否执行循环。

这是它的写法：

	# continue语句搭配for循环
	for...in...:
	    ...
	    if ...:
	        #满足continue语句，触发下一轮循环
	        continue
	    ...

-- --
	# continue语句搭配while循环
	while...(条件):
	    ...
	    if ...:
	        #满足continue语句，触发下一轮循环
	        continue
	    ...
我们看下下面这个例子：  

	current_number=0
	while current_number < 10:
	    current_number+=1#等同于current_number = current_number + 1
	    
	    #如果是偶数，则回到循环，如果是奇数，则打印出来
	    if(current_number%2==0):
	#%是求余数的除法，偶数除以2等于0，if条件成立，触发continue语句，跳回循环开头
	        continue
	    print(current_number)#if条件不成立，打印出奇数
	#所以输出是1 3 5 7 9
这个语句比较简单，大家可以自己在VS Code上写一写。
## pass语句
pass的意思是跳过，一般用来表示什么都不做，在实际中，有时还不知道增加什么语句时，可以先用pass占着。

	a = int(input('请输入一个整数:'))
	if a >= 100:
	    #如果a>=100，就什么都不做
	    #但是如果不写，会报错。因为if条件分支内部必须要有执行的语句
	    pass
	else:
	    print('你输入了一个小于100的数字')
OK，pass。pass语句就是这么简单。
## else语句
else语句咱们在条件判断里面学过，if else,if elif else。

这里我们要学习的是else配合循环语句的用法。

比如这样子：

	for i in range(5):
	    a = int(input('请输入0来结束循环，你有5次机会:'))
	    if a == 0:
	        print('你触发了break语句，循环结束，导致else语句不会生效。')    
	        break
	else:
	    print('5次循环你都错过了，else语句生效了。')
else语句要执行，那么它前面的for循环就不可以break。换句话说，只有for循环完全的执行了，else语句里面的内容才会被执行。

再看一个例子，else搭配while循环

	a = 0  # 用一个变量先创造它
	while a <3 : #while后面接判断语句，
	    password = int(input('请尝试输入密码')) #input默认返回一个字符串，
	#加上int（）转化为整数类型
	    a = a + 1 #a随着输入一次密码，a的值就加1
	    if password == 888 : #进入判断，记得判断用 ==
	        print('输入正确，您多多存款至本银行')
	        break #打破循环
	else : #while 可以搭配else，即当while条件不成立时，执行else语句
	    print('你已输入三次密码错误，请携带身份证和银行卡到银行网点报到吧。')

while 可以搭配else，即当while条件不成立时，执行else语句
