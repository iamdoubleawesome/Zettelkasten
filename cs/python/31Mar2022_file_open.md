#31Mar2022

# file open mode

## Example statement

- We have a file named `sample.txt` and inside it's

  ```tex
  Hello,
  This is Alice!
  ```

  and we are using the following commands
	for `read`
  ```python
  with open("sample.txt", mode) as f:
    f.read()
  ```
  and for `write`
  ```python
  with open("sample.txt", mode) as f:
    f.write("123")
  ````
  
- Also, we don't have a file named `not_there.txt`
  



# Features

- Read

- Write

- Create: it will create a file if it doesn't exist; otherwise,it will have error as follows:
  ```bash
  FileNotFoundError: [Errno 2] No such file or directory: 'not_there.txt'
  ```

- Truncate: it means it will clear the content when we write, in this case, `sample.txt` becomes

  ```tex
  123
  ```
  Otherwise, it becomes
  ```tex
  123lo,
  This is Alice!
  ```
  
- Initial position at start/end: initial pointer's position; for example, `write` with `r` gives
  ```tex
  123
  ```
  while `write` with `a` gives
  ```tex
  Hello,
  This is Alice!123
  ```

# Comparison table

| Features                  | `w`  | `r`  | `a`  | `w+` | `r+` | `a+` |
| ------------------------- | ---- | ---- | ---- | ---- | ---- | ---- |
| Read                      |      | O    |      | O    | O    | O    |
| Write                     | O    |      | O    | O    | O    | O    |
| Create                    | O    |      | O    | O    |      | O    |
| Truncate                  | O    |      |      | O    |      |      |
| Initial position at start | O    | O    |      | O    | O    |      |
| Initial position at end   |      |      | O    |      |      | O    |

# 







---

#python #io #file #open

---

Source:

- https://mkyong.com/python/python-difference-between-r-w-and-a-in-open