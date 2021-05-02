# 基础操作及命令

## 文件操作

### 打开文件
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
