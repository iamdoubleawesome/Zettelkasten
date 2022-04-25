#29Mar2022

# user defined class type

User defined class objects are instances of the object named `type`, which is itself a `class`.

However, when you put the bracket on, new instances of that `type` is made.

```python
class A:
  pass

print(type(A))
# <class 'type'> ## only create a `type` object, like `list`, `str`
print(type(A()))
# <class '__main__.A'>  ## create an object along with this class definition
```



---

#python #class #type

---

Source:

- https://docs.python.org/3/tutorial/classes.html