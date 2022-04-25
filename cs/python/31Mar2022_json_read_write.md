#31Mar2022

# json 

- read

  - `load`: deserialise a file
  - `loads`: deserialise a string or unicode 

  ```python
  import json
  with open("sample.json", 'r') as f:
    data = json.load(f)
    data = json.loads(f.read())
  ```

- write

  - `dump`: serialise into a `JSON` file
  - `dumps:` transfer  `dict` to a `JSON` string

  ```python
  import json
  with open("sample.json", 'w') as f:
    json.dump(data, f)
    f.write(json.dumps(data))
  ```

  