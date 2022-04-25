#29Mar2022

# First-Class Object

In python, all basic data types and function and class are all first-class object. Can be 

1. Assigned to an identifier;
2. Passed as a parameter;
3. Returned by a function.

## `class`

1. Assigned to an identifier;

   ```python
   class Hello:
       pass
   
   scream = Hello
   
   print(id(Hello), id(scream))
   # 140225515005504 140225515005504
   ```

   Same `id` means they are same object.

2. Passed as a parameter;

   ```python
   class Hello():
       def __init__(self):
           print('wow')
   
   if __name__ == "__main__":
       print(Hello())
   
   # wow
   # <__main__.Hello object at 0x10766e9d0>
   ```
   
3. Returned by a function.
   ```python
   class Hello():
       def __init__(self, x):
           print('wow',x)
   
   def hello(x):
       return Hello(x)
   
   if __name__ == '__main__':
       hello(5)
   
   # 5
   ```
   
   

---

#python #object #oop

---

source:

- Book: data structure and algorithms in python by Goodrich p47
- [28Mar2022_first_class_object](28Mar2022_first_class_object.md) about `function`
- 