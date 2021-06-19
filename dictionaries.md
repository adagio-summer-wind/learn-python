是python中的一种数据结构  
```python
dict = {'key1':5, 3:7, 'key2': 'she', 9:'he'}
>>> dict
{'key1': 5, 3: 7, 'key2': 'she', 9: 'he'}
```
# 特点  
1、看似无须无序实则有序  
字典中元素的位置与存储点先后顺序无关——无序  
字典中元素的位置由key的hash计算值决定——有序  
2、一个字典中key不能重复，value可以重复
3、字典会浪费比较大的内存，是一种以空间换时间的数据结构

# 结构  
1、元素结构： key: value  
key(键)：必须为不可变序列，如字符串，常数等  
value（值）：要求还未知，决大多数值都可以用  

# 使用
## 1、定义
```python
# 方式一
scores = {'张三':98, '李四':78, '王五':89}
>>> print(type(scores))
<class 'dict'>
>>> print(scores)
{'张三': 98, '李四': 78, '王五': 89}
# 方式二
scores_2 = dict(张三=98, 李四=67, 王五=89)
>>> print(scores_2)
{'张三': 98, '李四': 67, '王五': 89}
# 定义空字典
d1 = {}
d2 = dict()
```
## 2、查询字典元素的值
```python
scores = {'张三':98, '李四':78, '王五':89}
# 方式一： dictname[key]
scores['李四']
78

# 方式二： dictname.get(key)
>>> scores.get('李四')
78
# 区别，所查询元素在字典中不存在时才有
>>> scores['马六']
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: '马六'

>>> scores.get('马六')
>>> print(scores.get('马六'))    # 不存在时默认为None
None
print(scores.get('王五',100))
89
>>> print(scores.get('马六',100))   # 如果不存在，将默认值设为100
100
```
## 3、修改、删除字典元素
```python
scores = {'张三':98, '李四':78, '王五':89}
# 修改
scores['张三'] = 77
# 删除
del scores['李四']   # 删除特定元素

scores.clear()    # 清空字典
```
## 4、获取字典视图
```python
scores = {'张三':98, '李四':78, '王五':89}

>>> keys = scores.key()             # 获取字典的key
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'dict' object has no attribute 'key'
>>> keys = scores.keys()
>>> print(keys)
dict_keys(['张三', '李四', '王五'])
>>> print(type(keys))
<class 'dict_keys'>
>>> print(list(keys))
['张三', '李四', '王五']

>>> values = scores.values()        # 获取字典的values
>>> print(values)
dict_values([98, 78, 89])
>>> print(type(values))
<class 'dict_values'>

>>> items = scores.items()           # 获取字典的key-value对
>>> print(items)
dict_items([('张三', 98), ('李四', 78), ('王五', 89)])
>>> print(type(items))
<class 'dict_items'>
>>> print(list(items))                    # 转换之后的列表的元素是元组
[('张三', 98), ('李四', 78), ('王五', 89)]
```
## 5、遍历字典
```python
 for cha in scores:             # cha获取的是字典中的Key
...     print(cha, scores[cha])
...
张三 98
李四 78
王五 89

for score in scores.items():
...     print(score)
...
('张三', 98)
('李四', 78)
('王五', 89)
```
## 6、字典生成式
```python
items = ['fruits', 'books', 'others']
>>> prices = [96, 78, 85]
>>> dict = {item:price  for item,price in zip(items,prices)}   # zip()用于生成元组，即key-value对
>>> print(dict)
{'fruits': 96, 'books': 78, 'others': 85}
```
