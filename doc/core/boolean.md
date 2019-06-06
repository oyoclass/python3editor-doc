## Boolean

Booleans are used to show the logical truth values *True* and *False*.

### Constants

* True
* False

The following values are considered *False*: None, False, 0, 0.0, 0j, '', (), [], {}, set([])

### Convert Value to Boolean

* `bool(x)` : convert x to True or False

### Logical Operations

* `and` : x and y. This means that if x if false then x, else y
* `or` : x or y. This means that if x is false, then y, else x
* `not` : not x. Thsi means that if x is false, then True, else False

### Example

```python
print(True)              # True
print(1 < 2)             # True
print(2 > 3)             # False
print(3 <= 3)            # True
print(1 < 2 and 2 > 3)   # False
print(1 < 2 or 2 > 3)    # True
print(not 1 < 2)         # False
print(bool(0))           # False
print(bool([]))          # False
print(bool(3))           # True
```

### Reference

* Standard Types at [docs.python.org](https://docs.python.org/3.7/library/stdtypes.html)