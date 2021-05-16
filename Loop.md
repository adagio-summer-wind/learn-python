In Python, the process of repetitive execution of the same block of code is called an iteration.<br>
There are two types of iteration:

>Definite iteration, where the number of repetitions is stated in advance.<br>
>Indefinite iteration, where the code block executes as long as the condition stated in advance is true.

# for loop
syntax
```python
for variable in iterable:
    statement
```

常用形式
```python
for i in range(5):
    print(i)
    
for i in range(5, 45, 10):
    print(i)
>>>
5
15
25
35

# when not use the counter variable in your loop
for _ in range(100):
    do_smth()
```
