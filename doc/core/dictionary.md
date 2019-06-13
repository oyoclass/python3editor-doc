## Dictionary

Dictionaries are sometimes found in other languages such as “associative memories” and “associative arrays”. Unlike sequences, which are indexed by a range of numbers, dictionaries are indexed by keys, which can be any immutable type.

 It is best to think of a dictionary as an unordered set of key-value pairs, where all the keys must be unique. A pair of curly braces creates an empty dictionary: `{}`. When you place values in a dictionary, you must write the key-value pair like this: `key: value`. 

### Functions

* `dict.clear()` : Removes all items from the dictionary.
* `dict.get(key[, default])` : Returns the value for key if *key* is in the dictionary, else default. If *default* is not given, it defaults to **None**, so that this method never raises a `KeyError`.
* `key in dict`: Returns `True` if *d* has key *key*, else `False`.
* `dict.items()` : Returns a new view of the dictionary’s items (`(key, value)` pairs). 
* `dict.keys()` : Returns a new view of the dictionary’s keys.
* `dict.pop(key[, default])` : If *key* is in the dictionary, remove it and return its value, else return *default*. If *default* is not given and *key* is not in the dictionary, a `KeyError` is raised.
* `dict.setdefault(key[, default])` : If *key* is in the dictionary, return its value. If not, insert *key* with a value of *default* and return *default*. *default* defaults to `None`.
* `dict.update([other])` : Updates the dictionary with the key/value pairs from *other*, overwriting existing keys. Returns `None`.
* `dict.values()` : Returns a new view of the dictionary’s values.

### Example

```python
a = {"name": "Bo", "age": 20}
print("name" in a)                   # True
print(a.keys())                      # dict_keys(['name', 'age'])
print(a.values())                    # dict_values(['Bo', 20])
a.setdefault("gender", "m")         
print(a)                             # {'name': 'Bo', 'age': 20, 'gender': 'm'}
a.update({"city": "Stony Brook"})   
print(a)                             # {'name': 'Bo', 'age': 20, 'gender': 'm', 'city': 'Stony Brook'}
```

### Change from Python2
The `has_key(key)` function is no longer supported in Python3. 

### Reference

* [Dictionary as a Data Structure](https://docs.python.org/3/tutorial/datastructures.html#dictionaries) at *docs.python.org*
* [Dict as a Mapping Type](https://docs.python.org/3/library/stdtypes.html#mapping-types-dict) at *docs.python.org*

