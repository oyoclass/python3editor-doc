## What is Python3?

Quote from Python official website:

> Python is an easy to learn, powerful programming language. It has efficient high-level data structures and a simple but effective approach to object-oriented programming. Python’s elegant syntax and dynamic typing, together with its interpreted nature, make it an ideal language for scripting and rapid application development in many areas on most platforms.

Currently Python has two versions: Python2 and Python3. Python3 is the new version of Python. Quote from wikipedia:

> Python 3.0 (also called "Python 3000" or "Py3K") was released on December 3, 2008. It was designed to rectify fundamental design flaws in the language—the changes required could not be implemented while retaining full backwards compatibility with the 2.x series, which necessitated a new major version number. The guiding principle of Python 3 was: "reduce feature duplication by removing old ways of doing things".

Python2 won't be maintained after January 1, 2020. If you are new to programming, you should learn Python3 instead of Python2. However, if you are already familiar with Python2, learning Python3 will be also very easy to you.


## About OYOclass' Python3 Editor

Python3 Editor is an application built into the OYOclass platform which can be used to write Python3 code. OYOclass' Python3 Editor uses Python version 3.6 behind the scene. You can use any standard Python3 libraries in Python3 Editor, except the `Turtle` and `tkinter` graphic libraries. If you want to use the `Turtle` library with Python, check the "Python Mini" app on OYOclass platform.

The following links from Python's official website can help you get started.

* [The Python Tutorial](https://docs.python.org/3.6/tutorial/index.html)
* [The Python Language Reference](https://docs.python.org/3.6/reference/index.html)
* [The Python Standard Library](https://docs.python.org/3.6/library/index.html)


## Quick Start

Copy following example code to OYOclass' Python3 Editor then click the "Run" button:

#### Print

```python
print("Hello World")
print(123)
print(1 + 2)
print(1 + 2 * 3)
```

#### User Input

```python
name = input("What's your name?\n")
age = input("How old are you?\n")
print(f"Hello {name}, you are {age} years old")
```

#### Loop

```python
for i in range(1, 6):
    print("* " * i)
```

#### Call Web API

```python
from urllib.request import urlopen
import json

req = urlopen("https://aws.random.cat/meow")
data = json.loads(req.read())
print(f"Open the URL below, you will see a cat: \n{data['file']}")
```

## Moving from Python2 to Python3

Since Python3 broke backward compatibility, and much Python2 code does not run unmodified on Python3. If you are already familiar with Python2, the notes below can help you quickly start coding in Python3.

#### Strings

Python3 strings are Unicode, the `unicode()` function is gone.

In Python2:
```python
s = unicode(x)
```

In Python3:
```python
s = str(x)
```

Also, the string % operator is deprecated; use `format()` or `f`:

In Python2:
```python
i = 1
s = "abc"
mystr = "%d %s" % (i, s)
```

In Python3:
```python
i = 1
s = "abc"
mystr = "{} {}".format(i, s)
# or
mystr = f"{i} {s}"
```

#### Print

In Python2:
```python
print "a", "b", "c"
```

In Python3:
```python
print("a", "b", "c")
```

#### Numbers

In Python2:
```python
x = 5 / 2.0 # x = 2.5
x = 5 / 2 # x = 2
```

In Python3:
```python
x = 5 / 2 # x = 2.5
x = 5 // 2 # x = 2
```

#### Exceptions

Catching exception objects requires the `as` keyword.

In Python2:
```python
try:
    process()
except Exception, ex:
    print ex
```

In Python3:
```python
try:
    process()
except Exception as ex:
    print(ex)
```

#### Renamed modules

* Python2 `import SimpleHTTPServer` ; Python3 `import http.server`
* Python2 `import ConfigParser` ; Python3 `import configparser`
* Python2 `import SocketServer` ; Python3 `import socketserver`
* Python2 `import Tkinter` ; Python3 `import tkinter`
* Python2 `import urllib` ; Python3 `import urllib.request, urllib.parse, urllib.error`
* Python2 `import urllib2` ; Python3 `import ullib.request, urllib.error`
* Python2 `import urlparse` ; Python3 `import urllib.parse`

Please notice that above doesn't include all differences between Python2 and Python3. To master Python3, you still need to read Python3's official documentations.


## Beyond OYOclass' Python3 Editor

If you would like to do more with Python and go beyond the capabilities of OYOclass' Python3 Editor, please download and install the Python:

* [Download Python](https://www.python.org/downloads/) : The version you download from Python's website most likely >= 3.7, although OYOclass' Python3 Editor uses Python3.6 behind the scene, there are not many differences with Python 3.7.
* [Python3 Official Documentation](https://docs.python.org/3/)
* [Automated Python 2 to 3 code translation](https://docs.python.org/3/library/2to3.html)
* [Six Library](https://pypi.org/project/six/) : Six is a Python 2 and 3 compatibility library. It provides utility functions for smoothing over the differences between the Python versions with the goal of writing Python code that is compatible on both Python versions. See the documentation for more information on what is provided.
* [Resources in Awesome Python Repository](https://github.com/vinta/awesome-python)