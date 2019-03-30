## File operations
* file is a storage format where we store information on the computer.
* It might text files like music, video, code and other stuff or binary
  files which are only understood able by computer.
* By using Python, we can easily manipulate these files.
* let's create a file names.txt and add few names.
* mode of files based on purpose
* r - read the content of file, setted default
* w - write the content to file, if file is not there it will create it.
* a - append contents to the file.
```
>>> names_list = ['chandan', 'nikhil']
>>> data = open('names.txt', 'w')
>>> for i in names_list:
...     data.write(i)
... 
7
6
>>> data.close()
>>> data = open('names.txt', 'r')
>>> data.read()
'chandannikhil'
>>> data.close()
>>> data = open('names.txt', 'a')
>>> data.write('\nBhavin gandahi')
15
>>> data.close()
>>> data = open('names.txt')
>>> data.read()
'chandannikhil\nBhavin gandahi'
>>> data.readline()
''
>>> with open('foo.txt', 'w') as f:
...     f.write("This is awesome")
... 
```

## Python Modules
* Python provides a rich support of modules.
* Modules/library are a collection of python scripts which can be reusable for writting complex program.
* We can import a module using import keyword.
* If it is not available it will give import error.
* dir() method tells what these modules provides.
```
>>> import math
>>> dir(math)
['__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'copysign', 'cos', 'cosh', 'degrees', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'pi', 'pow', 'radians', 'remainder', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc']
>>> math.e
2.718281828459045
>>> import platform
>>> platform.python_version()
'3.7.3'
>>> help('modules')
>>> import foo
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ModuleNotFoundError: No module named 'foo'
>>> import random
>>> random.randint(1, 100)
79
``` 
* A python script foo.py can be called as a module by using foo.py

## Exceptions
While writting programs, Errors are prone to occur. But It can be handled via
exception.
For example, we were trying to import a module but it was not there.
we can by pass this error by using try and except.
With try keyword, we do something, then in except clause once this
exception comes we do something else
```
>>> import sys
>>> def linux_interaction():
...     assert ('linux' in sys.platform), "Function can only run on Linux systems."
...     print('Doing something.')
... 
>>> try:
...     linux_interaction()
... except AssertionError as error:
...     print(error)
... else:
...     print('Executing the else clause.')
... 
Doing something.
Executing the else clause.
>>> 
```

## Writting simple CIL script
* We write scripts in order to reuse it multiple times.
* In python you see '__' double underscore aka dunder.
* create a script greetings.py
```
[raukadah@ironman python-workshop]$ python3 fun.py 
Welcome FOSS MEET
the value of __name__ is greetings
[raukadah@ironman python-workshop]$ cat greetings.py 
#!/usr/bin/python3
import sys

def greeting(name):
    print("Welcome {0}".format(name))
    print("the value of __name__ is {0}".format( __name__))

if __name__ == "__main__":
    name = "Chandan Kumar"
    greeting(name)
[raukadah@ironman python-workshop]$ cat fun.py 
#!/usr/bin/python3

import greetings
greetings.greeting('FOSS MEET')
[raukadah@ironman python-workshop]$ python3 fun.py 
Welcome FOSS MEET
the value of __name__ is greetings
[raukadah@ironman python-workshop]$
```

## Installing a new python module
$ python3 -m pip install requests