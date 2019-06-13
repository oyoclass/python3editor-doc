## List

Lists are used to group together values. They consist of a group of values or items, separated by commas, between square brackets. Lists might contain items of different types, but usually the items in a list have the same type.

The index in a list starts at 0, and you can visit last element using index -1.

```python
a = [1, 5, 2, 3]
print(a[0])          # 1
print(a[1])          # 5
print(a[-1])         # 3
print(a[1:3])        # Get elements from index 1 to index 3 (exclusive), i.e. [5, 2]
```

Change the element at a index:

```python
a = [1, 5, 2, 3]
a[1] = 7
print(a)             # [1, 7, 2, 3]
```

To check if an element is in a list, you can use the `in` operator:

```python
a = [1, 5, 2, 3]
print(5 in a)       # True
```

Use the `len` function to get the length (number of elements) of a list:

```python
a = [1, 5, 2, 3]
print(len(a))       # 4
```

### Functions for Lists

* `list.append(x)`
* `list.count(x)`
* `list.extend(L)`
* `list.index(x)`
* `list.insert(i, x)`
* `list.pop([i])`
* `list.remove(x)`
* `list.reverse()`
* `list.sort(cmp=None, key=None, reverse=False)`

For instructions on how to use these functions, check out [list functions](https://docs.python.org/3/tutorial/datastructures.html#more-on-lists) in Python's official documentation.

#### Example

```python
a = [1, 5, 2, 3]
a.append(6)
print(a)             # [1, 5, 2, 3, 6]
print(a.count(5))    # 1
a.remove(2)
print(a)             # [1, 5, 3, 6]
a.reverse()
print(a)             # [6, 3, 5, 1]
a.sort()
print(a)             # [1, 3, 5, 6]
```

## Tuple

Tuples are similar to lists. The main difference is that lists are mutable and tuples are immutable. Once you define a tuple within parentheses `()`, you can not change the elements of the tuple.

```python
b = (1, 5, 2, 3)
b.append(6)     	# This will give an error, since b is a tuple and immutable.
```

## Conversion between Tuple and List

Although a tuple cannot be changed, you can convert it to list, make changes, and then convert it back to tuple. You can do this with the `tuple` and `list` functions.

```python
b = (1, 5, 2, 3)
b = list(b)          # Convert tuple to list
b.append(6)          # Change list - append one more element
b = tuple(b)         # Convert list to tuple
print(b)             # (1, 5, 2, 3, 6)
```

### Reference

* [Introduction of Lists](https://docs.python.org/3/tutorial/introduction.html#lists) on *docs.python.org*
* [More on Lists](https://docs.python.org/3/tutorial/datastructures.html#more-on-lists) on *docs.python.org*