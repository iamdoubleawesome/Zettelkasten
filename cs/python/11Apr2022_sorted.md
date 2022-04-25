#11Apr2022

# `sorted`

`sorted(iterable, /, *, key=None, reverse=False)`

- `iterable` includes strings, list, tuples, sets, dictionaries and etc.
- `key` specifies a **function** (or other callable) to be called on each element prior to making comparisons
- `reverse`: boolean 
- Return a new sorted list from the items in `iterable`

```python
a="abcDEF"

print(sorted(a))
# ['D', 'E', 'F', 'a', 'b', 'c']

print(sorted(a, key=str.lower))
# ['a', 'b', 'c', 'D', 'E', 'F']
```





---

#python #iterable #sort

---

source:

- https://docs.python.org/3/library/functions.html#sorted
- https://docs.python.org/3/howto/sorting.html#sortinghowto