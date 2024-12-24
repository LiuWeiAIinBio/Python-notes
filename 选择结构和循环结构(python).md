@[toc]
# 选择结构
    # if语句、else语句后面要有冒号
    # if-else里面可以嵌套
    score = int(input("请输入成绩："))
    if 0 <= score <=100:
        if score >=60:
            print("及格")
        else:
            print("不及格")
    else:
        print("输入不合法")
***
# 循环结构
 1. while: 未知循环次数 
 2. for: 循环次数已知 
 3. break: 结束本层循环，返回到本层循环之外 
 4. continue:跳过continue后面的语句，但并不结束本层循环，而是重新判断是否进入本层循环的下一次循环。
 5. **for/while循环的else扩展模式:** 
```python
# else在while循环的内部，传统用法
n = int(input("请输入一个正整数："))
while n > 1:
	if n % 2 == 0:
		n = n/2
	else:
		n = 3 * n + 1
	print(n)

# else在while循环的外部，for/while循环的else扩展模式: 
# 当循环正常结束(非break结束)时，程序会继续执行else后面的语句块2
# 当break使循环结束时，程序不会继续执行else后面的语句块2
while <条件表达式>:
	<语句块1>
else:
	<语句块2>
            
for <循环变量> in <可迭代对象>:
	<语句块1>
else:
	<语句块2>

# 这段代码的目的是确保输入的标识符不以数字开头，并且只包含字母、数字和下划线。
# 如果标识符满足这些条件，程序会打印"yes"；
# 如果标识符以数字开头或包含其他字符，程序会打印"no"。
identifier = input()
for ch in identifier:
    if ch.isalpha() or ch.isdigit() or ch == "_":
    	continue
    else:
    	print("no")
    	break  # 跳出循环
else:
    if identifier[0].isdigit():
        print("no")
    else:
        print("yes")
```
