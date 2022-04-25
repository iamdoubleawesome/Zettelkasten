#29Mar2022

# Parentheses 

`function` or `method` is not processed when only call identifier but it will once add parentheses in. Ie, just `code`, but once add `()` we create an object. 

```python
def hello():
  print("hello")
	return "yes"

print(hello)
# <function hello at 0x109ca9160>
print(hello())
# hello
# yes
```

`class` without parentheses is just a `type` object but with will become an object instantiated from the `type`. Related to [`type`](29Mar2022_type) and [user defined class](29Mar2022_user_defined_class_type.md)

```python
def echo_bar(self):
    print(self.bar)
    return "hello" + str(self.bar)
h = type('Foo', (), {"bar": True, "echo_bar": echo_bar})

print(h)
# <class '__main__.Foo'>

print(h())
# <__main__.Foo object at 0x109baf7c0>
```

---

#python #parentheses #function #class #type

---

Source:

- [`type`](29Mar2022_type)  
- [user defined class](29Mar2022_user_defined_class_type.md)