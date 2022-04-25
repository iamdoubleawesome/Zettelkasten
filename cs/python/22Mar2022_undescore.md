

#22Mar2022

# Double/single underscore in python

- Single underscore before: suggests internal use 

- Single underscore after: to differ with Python built-in names, for example `class_`

- Double underscores before: create on attribute would differ in subclasses, for example:

- - `__colour` in class `Car` will make `_Car__colour` 
  - `SmallCar(Car)` will make an attribute `_SmallCar_colour`

- Double underscores before and after: overwrite special methods; for example

- - `__init__`
  - `__str__`
  - `__call__`
  - `__add__`

---

#python #underscore

---

source: [medium](https://towardsdatascience.com/whats-the-meaning-of-single-and-double-underscores-in-python-3d27d57d6bd1)

