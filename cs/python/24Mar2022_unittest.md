#24Mar2022

# `unittest '__init__ '`
## error
```python
# TypeError: __init__() takes exactly 1 argument (2 given)
```



## reason

class `unittest.TestCase`'s initialiser only takes **one** positional argument `self`, if we overwrite it, it will give error.



## fix

Instead of overwriting `'__init__'`, we shall introduce 
```python
def setUpClass():
    # whatever you want to define
```

---

#python #unittest

---

source: 
- https://stackoverflow.com/questions/42288747/init-takes-one-argument-2-given-unittest