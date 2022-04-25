#30Mar2022

# Variable

With `$` before identifier, it will refer to actual value, but without it will refer to identifier.

So if we want replace the value of same identifier

```bash
a=0
a=1
```

But not 

```bash
a=0
$a=1
# command not found: 0=1
```



However, if we want to refer value, we need to use

```bash
a=0
echo $a
```

Instead of 

```bash
a=0
echo a
# a
```



---

#bash #varbable 