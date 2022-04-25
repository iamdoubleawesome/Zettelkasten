#11Apr2022

# dict update

`dict.update([other])`

- Parameter can be another dict or a list of tuples, which are key/value pairs
- If nothing passed in parameter, the dict remains unchanged
- Returns `None`

```python
a = {"1": "1"}
b = {"2": "2"}
c = [("3", "3")]

print(a.update(b))
# None
print(a)
# {'1': '1', '2': '2'}

a.update(c)
print(a)
# {'1': '1', '2': '2', '3': '3'}
```

---

#python #dict #update

---

Source:

- https://www.programiz.com/python-programming/methods/dictionary/update