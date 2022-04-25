#29Mar2022

# Create `metaclass`

See definitions of [`metaclass`](29Mar2022_metaclass) first.

Here are all `python3`.



## set the `metaclass`

```python 
class Foo(metaclass=something, kwarg1=value1, kwarg2=value2)
```

Where:

- `something` is defined `metaclass`
- `kwarg1` and `kwarg2` are keyword arguments of `metaclass` while `value1` and `value2` are attributes



## custom `metaclass`

- Purpose: to change the class automatically when it's created
- Normally used in `APIs` to match the contents

### example: all classes in a module need to have their attributes in UPPERCASE

- We can set up `metaclass` in module level

- `metaclass` can be anything `callable`, ie doesn't need to be a `class` but also can be a `function`

#### start with `metaclass` as a function

```python
def upper_attr(future_class_name, future_class_parents, future_class_attrs):
    upperclass_attrs = {
    		attr if attr.startswith("__") else attr.upper(): v \
    		for attr, v in future_class_attrs.items()
    		}
    # still let `type` to do the class creation
    return type(future_class_name, future_class_parents, upperclass_attrs)

class Foo(metaclass=upper_attr):
    bar = 'bip'

print(hasattr(Foo, 'bar'))
# False
print(hasattr(Foo, 'BAR'))
# True
```

#### implement `metaclass` as a class

- Which means we could inherit from `type` class

```python
class UpperAttrMetaClass(type):
    def __new__(upperattr_metaclass, future_class_name, future_class_parents, future_class_attrs):
        upperclass_attrs = {
            attr if attr.startswith("__") else attr.upper(): v \
            for attr, v in future_class_attrs.items()
            }
        return type(future_class_name, future_class_parents, upperclass_attrs)
```

We can simplify the parameters' name as:

```python

class UpperAttrMetaClass(type):
    def __new__(cls, clsname, bases, attrs):
        upperclass_attrs = {
            attr if attr.startswith("__") else attr.upper(): v \
            for attr, v in future_class_attrs.items()
            }
        return type(cls, clsname, bases, upperclass_attrs)
```

`cls` in `__new__` is like `self` in `__init__`, always receives the class it's defining as the first parameter. And we can make it more `OOP`.

```python

class UpperAttrMetaClass(type):
    def __new__(cls, clsname, bases, attrs):
        upperclass_attrs = {
            attr if attr.startswith("__") else attr.upper(): v \
            for attr, v in future_class_attrs.items()
            }
        return type.__init__(cls, clsname, bases, upperclass_attrs)
```



#### why class instead of just a function?

- You can use `OOP`: inherit from `metaclass`, override parent methods, `metaclass` can use `metaclass`
- Subclasses of a class will be instances of its `metaclass` if you specified a metaclass-class, but not with a metaclass-function. (Need to come back)



# When do we use?

- Example: `django` ORM

```python
class Person(models.Model):
    name = models.CharField(max_length=30)
    age = models.IntegerField()
```

But if you do 

```python
person = Person(name='bob', age='35')
print(person.age)
```

It will return `int` object but not `IntegerField` object. This should hidden in `metaclass`.

---

#python #metaclass #class #type

---

source:

- https://stackoverflow.com/questions/100003/what-are-metaclasses-in-python