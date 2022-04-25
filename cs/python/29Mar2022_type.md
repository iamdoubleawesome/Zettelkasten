#29Mar2022

# type

- `type` can return the type of object
- `type` can create a class, give description
- `type` is the built-in `metaclass` of python to create all classes



## return type of the object

```python
print(type("1"))
# <class 'str'>

print(type(1))
# <class 'int'>

class Hello:
    def __init__(self):
        print('wow')

def hello(x):
    return Hello(x)

if __name__ == '__main__':
    print(type(hello))
    # <class 'function'> ## didn't excute function
    print(type(Hello))
    # <class 'type'> ## user-defined class objects are instances of the object name
    print(type(Hello()))
    # wow ##excute the class
    # <class '__main__.Hello'>
```



## return a class, given descriptions of a class

`type(name, bases, attrs)` where:

- `name`: name of the class
- `bases`: tuple of the parent class, could be empty, for inheritance 
- `attrs`: dictionary containing attributes name and values

```python
class Foo():
  bar = True
  def echo_bar(self):
    print(self.bar)
```

Is same as

```python
def echo_bar(self):
    print(self.bar)
    return "hello" + str(self.bar)
h = type('Foo', (), {"bar": True, "echo_bar": echo_bar}) 
```

In this case class can share same string of `name` and `identifier`, just need to be `Foo = type('Foo', (), {"bar": True, "echo_bar": echo_bar}) `. Stating here differently to emphasis they could be different things. 

Also, using `class Foo` or `class Foo()` will automatically have an `identifier` as `Foo`, no need to assign like `h = type(...)`.

```python
print(h.echo_bar)
# <function echo_bar at 0x10f1c5160>
```

And we can also instantiate this class, 

```python
f = h()
print(f.echo_bar)
# <bound method echo_bar of <__main__.Foo object at 0x10f2d29d0>>
print(f.echo_bar())
# True
# helloTrue
```



---

#python #type #class #metaclass

---

Source: 

- https://stackoverflow.com/questions/100003/what-are-metaclasses-in-python
- [metaclass](29Mar2022_metaclass)

