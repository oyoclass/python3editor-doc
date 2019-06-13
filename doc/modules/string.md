## string - Common String Operations

The string module contains useful constants and functions.

### Constants

* `string.ascii_letters` : The concatenation of the **ascii_lowercase** and **ascii_uppercase** constants described below.
* `string.ascii_lowercase` : The lowercase letters *abcdefghijklmnopqrstuvwxyz*. This value is not locale-dependent and will not change.
* `string.ascii_uppercase` : The uppercase letters *ABCDEFGHIJKLMNOPQRSTUVWXYZ*. This value is not locale-dependent and will not change.
* `string.digits` : The string *0123456789*.
* `string.hexdigits` : The string *0123456789abcdefABCDEF*.
* `string.letters` : The concatenation of the strings lowercase and uppercase described below.
* `string.octdigits` : The string *01234567*.
* `string.punctuation` : String of ASCII characters that consist of punctuation characters.
* `string.printable` : String of characters which are considered printable. This is a combination of digits, letters, punctuation, and whitespace.
* `string.whitespace` : A string containing all characters that are considered whitespace.

### Helper Functions

* `string.capwords(s[, sep])`: Splits the argument into words using `str.split()`, capitalizes each word using `str.capitalize()`, and joins the capitalized words using `str.join()`.  

### Example

```python
import string

print(string.ascii_letters)
# abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
print(string.ascii_lowercase)
# abcdefghijklmnopqrstuvwxyz
print(string.punctuation)
# !"#$%&'()*+,-./:;<=>?@[\]^_`{|}~

s = "hello world"
print(string.capwords(s))
# Hello World
```


### Reference

* [String Module](https://docs.python.org/3/library/string.html) at *docs.python.org*