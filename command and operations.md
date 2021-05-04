# 基础操作及命令

目录
## 1、文件操作
### >1.1打开文件（写入和读取）
## 2、类class
### >2.1 类的定义
### >2.2 类的使用
### >2.3 类
## 3、元组（tuple） 列表（list）
### >3.1 定义
### >3.2 操作
### >3.3 多维数组
## 4、dictionary

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
### 3.1 定义
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
### 3.2 操作
```python
a_list = [47,55,33,0,47]
print(a_list)

a_list.append(0)
print("在最后添加'0':", a_list)
a_list.insert(1, 0)
print("在1位置处插入‘0’:", a_list)
a_list.remove(0)
print("移除第一个‘0’:", a_list)

print("输出最后一个：", a_list[-1])
print("输出索引0—2的值：", a_list[:3])
print("输出索引2—3的值：", a_list[2:4])

a_list.index(0)
a_list.count(0)
a_list.sort()
print("顺序排列：", a_list)
a_list.sort(reverse=True)
print("倒序排列：", a_list)

>>>
[47, 55, 33, 0, 47]
在最后添加'0': [47, 55, 33, 0, 47, 0]
在1位置处插入‘0’: [47, 0, 55, 33, 0, 47, 0]
移除第一个‘0’: [47, 55, 33, 0, 47, 0]
输出最后一个： 0
输出索引0—2的值： [47, 55, 33]
输出索引2—3的值： [33, 0]
顺序排列： [0, 0, 33, 47, 47, 55]
倒序排列： [55, 47, 47, 33, 0, 0]
```
### 3.3 多维数组
```python
multi_a = [[1,2,3],
           [4,5,6],
           [7,8,9]]
print(multi_a[1][1])           
```
更多使用见numpy库的使用

## 4、dictionary
```python
def function():
    print('a function')

d = {'apple':1,'pear':2, 'orange':3 }
d2 = {1:[1,2,3], 2:{1:'one', 2:'two', 3:'three'}, 'f':function}

print(d['pear'])
print(d2[1], d2[2])

d2['f']()

del d['pear']
print(d)
d[4] = 'four'
print(d)

>>>
2
[1, 2, 3] {1: 'one', 2: 'two', 3: 'three'}
a function
{'apple': 1, 'orange': 3}
{'apple': 1, 'orange': 3, 4: 'four'}
```
