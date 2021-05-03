# 基础操作及命令

目录
## 1、文件操作
### >1.1打开文件（写入和读取）
## 2、类class
### >2.1 类的定义
### >2.2 类的使用
### >2.3 类
## 3、元组（tuple） 列表（list）

## 1、文件操作
### >1.1打开文件
1、向打开的文件写入
```python
text = 'This is my first test.\nThis is the second line.'

my_file = open('my file.txt','w')  # 打开文件my file.text
                                # syntax: varible = open('filename.type','打开形式w/r等')
my_file.write(text)          
my_file.close()          # 完成操作后要关闭文件，否则会出现错误
# 文件my file.txt必须存在且位于程序文件夹中才能打开；文件以w（写）的形式打开才能进行写操作
```
2、在打开的文件中添加内容
```python
append_text = '\nThis is an appended file'

my_file = open('my file.txt','a')  # 以appended的形式打开文件
my_file.write(append_text)
my_file.close()
```
3、读取文件内容
```python
file = open('my file.txt','r')  # 以r读的方式打开
content = file.read()           # 读取全部内容
print(content)
file.close()
# 按行读取
file = open('my file.txt','r')
content = file.readline()
print(content)
content = file.readline()
print(content)
file.close()
# 按行读取为列表
file = open('my file.txt','r')
content = file.readlines()
print(content)
```

## 2、类class
### >2.1 类的定义
```python
class Calculator:                 # syntax:   class classname:
  name = 'Good calculator'        #              define 类的属性
  price = 18
                                  #              define functions
  def add(self,x,y):              #              def functionName1(self,parameter1,……，parameterN):
     print(self.name)             #                 具体内容
     result = x + y               #                 以 “self.属性名” 的形式在函数内部调用定义的属性
     print(result)  
  def minus(self,x,y):            #              def functionName2(self,parameter1,……，parameterN):
     result = x - y               #                  具体内容
     print(result)
  def times(self,x,y):
     result = x * y
     print(result)
  def divide(self,x,y):
     result = x / y
     print(result)
```
### >2.2 类的使用
```python
cal = Calculator()      #Calculator()中的（）不能省略
print(cal.name)
cal.add(7,9)
```
```python
cal1 = Calculator
cal2 = Calculator()
print(cal1,cal2)
# 输出：<class '__main__.Calculator'> <__main__.Calculator object at 0x00000265B798FD88>
# 一个是类的名称，另一个是该类对象
```
### >2.3 类init
```python
class Calculator:                    
    def __init__(self,name,price,hight=18,width=8):
        self.name = name
        self.p = price
        self.hight = hight
        self.w = width  
```
```python
 c = Calculator('calculator', 10, width = 3)
>>> c.w
3
```
## 3、元组（tuple） 列表（list）
```python
a_tuple = (56,47,2,9)
a_list = [47,55,33]

for index in range(len(a_tuple)):
    print('index:',index, 'a_tuple[index]:',a_tuple[index])

    
for i in range(len(a_list)):
    print('index:',i, 'a_list[i]:',a_list[i])
```

元组和列表的区别？？？  
定义：
>元组使用（）  
>列表使用 []
