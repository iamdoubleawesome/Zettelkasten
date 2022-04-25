#28Mar2022

# First-Class Object

In python, all basic data types and function and class are all first-class object. Can be 

1. Assigned to an identifier;
2. Passed as a parameter;
3. Returned by a function.

## `function`

1. Assigned to an identifier;

   ```python
   scream = print
   scream("hello")
   # hello
   print(id(scream), id(print))
   # 4505004928, 4505004928
   ```

   Same `id` means they are same object.

2. Passed as a parameter;

   ```python
   def scream(a):
       print(a)
   
   def hello(func, x):
       func(x)
   
   if __name__ == '__main__':
       hello(scream, 5)
   
   # 5
   ```

3. Returned by a function.
   ```python
   def hello(x):
       def scream(a):
           return a + 5
       return scream(x)
   
   if __name__ == '__main__':
       print(hello(5))
   
   # 10
   ```

   

---

#python #object #oop

---

source:

- Book: data structure and algorithms in python by Goodrich p47
- [28Mar2022_first_class_object](../general/28Mar2022_first_class_object.md) in general
- https://zhuanlan.zhihu.com/p/21329577