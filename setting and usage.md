对于Windows系统
# 使用python编译环境
1、IDLE<br>
2、python 命令提示符窗口<br>
方式一：<br>
>直接使用python自带的命令提示符窗口

方式二：<br>
>从系统Command Prompt进入<br>
>查询已经安装的python版本<br>
>```cmd
>python -V
>```
>进入python编译器环境<br>
>```cmd
>python
>```
>退出python编译环境，返回系统Command Prompt<br>
>按`Ctrl+Z`, 然后`ENTER` 
>或者使用`exit()`命令

3、系统命令提示符窗口执行python文件<br>
方式一：<br>
>使用`cd(change directory)`进入文件所在文件夹
>```cmd
>cd 路径
>```
>然后输入执行文件执行
>```cmd
>python filename.py
>```

方式二：<br>
>直接将要执行的python文件拖入CMD窗口

方式三：<br>
>直接双击文件

# cmd窗口常用指令
```cmd
# 系统

# 查看已安装的python版本
py --version
py -V

# 查看已安装的pip版本
py -m pip --version

# 从标准库中引导pip
py -m ensurepip --default-pip

# 安装更新pip
python get-pip.py   # 会同时安装setuptools和wheel
python get-pip.py --prefix=/usr/local/  # 安装到指定位置
python3 -m pip install --upgrade pip setuptools wheel # 安装和更新pip
```

## Virtual Environment<br>
It have their own installation directories and they don’t share libraries with other virtual environments.
```cmd
py -m venv tutorial_env
tutorial_env\Scripts\activate    # 在tutorial_env中创建一个新的virtual environment,
                                 # 并将其设置为当前窗口的默认python环境

# 使用venv
py -m venv <DIR>
<DIR>\Scripts\activate
# 使用virtualenv
virtualenv <DIR>
<DIR>\Scripts\activate
```
## 使用pip安装python package
```cmd
py -m pip install "SomeProject"
py -m pip install "SomeProject==1.4"
py -m pip install "SomeProject>=1,<2"
py -m pip install "SomeProject~=1.4.2"

py -m pip install --upgrade SomeProject  # 更新升级package
```

# How to install a modules
  关键点：命令提示符窗口的使用方式
  
  
![image](https://github.com/adagio-summer-wind/learn-python/blob/notes/images/cmd%E7%AA%97%E5%8F%A3.jpg)

保证在用户文件下或其它指定文件（具体我也不知道）下进行操作，必须先进入一个文件夹，然后输入指令  
python -m pip install module's name  
上图中安装的是numpy
