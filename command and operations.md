# 基础操作及命令

## 文件操作

### 打开文件
```python
text = 'This is my first test.\nThis is the second line.'

my_file = open('my file.txt','w')  # 打开文件my file.text
                                # syntax: varible = open('filename.type','打开形式w/r等')
my_file.write(text)          
my_file.close()          # 完成操作后要关闭文件，否则会出现错误
# 文件my file.txt必须存在且位于程序文件夹中才能打开；文件以w（写）的形式打开才能进行写操作
```
