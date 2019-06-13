## What is Python3?

Quote from Python's official website:

> Python is an easy to learn, powerful programming language. It has efficient high-level data structures and a simple but effective approach to object-oriented programming. Python’s elegant syntax and dynamic typing, together with its interpreted nature, make it an ideal language for scripting and rapid application development in many areas on most platforms.

Currently Python has two versions: Python2 and Python3. Python3 is the new version of Python. Quote from wikipedia:

> Python 3.0 (also called "Python 3000" or "Py3K") was released on December 3, 2008. It was designed to rectify fundamental design flaws in the language—the changes required could not be implemented while retaining full backwards compatibility with the 2.x series, which necessitated a new major version number. The guiding principle of Python 3 was: "reduce feature duplication by removing old ways of doing things".

Python2 won't be maintained after January 1, 2020. If you are new to programming, you should learn Python3 instead of Python2. However, if you are already familiar with Python2, learning Python3 will be very easy for you.


## About OYOclass' Python3 Editor

The Python3 Editor is an application built into the OYOclass platform, which can be used to write Python3 code. OYOclass' Python3 Editor uses Python version 3.6 behind the scenes. You can use any of the standard Python3 libraries in Python3 Editor, except the `Turtle` and `tkinter` graphic libraries. If you want to use the `Turtle` library with Python, check out the **Python Mini** app on OYOclass platform.

The following links from Python's official website can help you get started.

* [The Python Tutorial](https://docs.python.org/3.6/tutorial/index.html)
* [The Python Language Reference](https://docs.python.org/3.6/reference/index.html)
* [The Python Standard Library](https://docs.python.org/3.6/library/index.html)


## Quick Start

Copy the following code samples to OYOclass' Python3 Editor. Then, click the "Run" button.

**Print**

```python
print("Hello World")
print(123)
print(1 + 2)
print(1 + 2 * 3)
```

**User Input**

```python
name = input("What's your name?\n")
age = input("How old are you?\n")
print(f"Hello {name}, you are {age} years old")
```

**Loop**

```python
for i in range(1, 6):
    print("* " * i)
```

**Call Web API**

```python
from urllib.request import urlopen
import json

req = urlopen("https://aws.random.cat/meow")
data = json.loads(req.read())
print(f"Open the URL below, you will see a cat: \n{data['file']}")
```

## Beyond OYOclass' Python3 Editor
  
If you would like to do more with Python and go beyond the capabilities of OYOclass' Python3 Editor, please download and install the Python:

* [Download Python](https://www.python.org/downloads/): The version you download from Python's website is most likely greater than or equal to version 3.7. Although OYOclass' Python3 Editor uses Pythonv3.6 behind the scenes, there are not many differences between Python 3.6 and Python 3.7.
* [Python3's Official Documentation](https://docs.python.org/3/)
* [Automated Python 2 to 3 code translation](https://docs.python.org/3/library/2to3.html)
* [Six Library](https://pypi.org/project/six/): Six is a Python 2 and 3 compatibility library. It provides utility functions to smooth over the differences between the Python versions. The goal is to write Python code that is compatible in both Python versions. See the documentation for more information on what is provided.
* [Resources in Awesome Python's Repository](https://github.com/vinta/awesome-python)

** Renamed modules**

* Python2 `import SimpleHTTPServer` to Python3 `import http.server`
* Python2 `import ConfigParser`     to Python3 `import configparser`
* Python2 `import SocketServer` 	to Python3 `import socketserver`
* Python2 `import Tkinter` 			to Python3 `import tkinter`
* Python2 `import urllib` 			to Python3 `import urllib.request, urllib.parse, urllib.error`
* Python2 `import urllib2` 			to Python3 `import ullib.request, urllib.error`
* Python2 `import urlparse` 		to Python3 `import urllib.parse`

