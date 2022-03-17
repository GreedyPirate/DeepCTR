# python基础

## __init__和__new__
new是在创建对象实例之前钓鱼，返回创建的对象实例
init是在创建对象实例之后，对成员变量初始化

## 具名元组 namedtuple
```python
from collections import namedtuple
Student = namedtuple("_Student","name,age sex like")
zhangsan = Student("张三",15,"男","打篮球")
print(zhangsan,zhangsan.name,zhangsan.age,zhangsan.sex,zhangsan.like,sep="\n")
```

## dict
### OrderedDict
插入时带顺序的hashmap

### defaultdict()
创建一个value为list的字典
```python
from collections import defaultdict
result = defaultdict(list)
data = [("p", 1), ("p", 2), ("p", 3),
        ("h", 1), ("h", 2), ("h", 3)]
 
for (key, value) in data:
    result[key].append(value)
# {p:[1,2,3], h:[1,2,3]}
```