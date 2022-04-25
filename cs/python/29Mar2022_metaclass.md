#29Mar2022

# metaclass

- We define classes to create objects
- But `class` is also an object
- `metaclass` is used to create `class`
- `type` is a `metaclass` to create all of the classes



```python
age = 35
print(age.__class__)
# <class 'int'>

name = 'alice'
print(name.__class__)
# <class 'str'>

def foo(): pass
print(foo.__class__)
# <class 'function'>

class Bar(): pass
print(Bar.__class__)
# <class 'type'>

b = Bar()
print(b.__class__)
# <class '__main__.Bar'>
```



```python
print(age.__class__.__class__)
print(name.__class__.__class__)
print(foo.__class__.__class__)
print(Bar.__class__.__class__)
print(b.__class__.__class__)

# <class 'type'>
# <class 'type'>
# <class 'type'>
# <class 'type'>
# <class 'type'>
```



---

#python #metaclass #class #type

---

source:

- https://stackoverflow.com/questions/100003/what-are-metaclasses-in-python