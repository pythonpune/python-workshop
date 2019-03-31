# The Beginning

## [Using Python interpreter](https://docs.python.org/3/tutorial/interpreter.html)

* Type `python3` command in terminal to open a Python Interpreter.

```
[raukadah@ironman python-workshop]$ python3
Python 3.7.3 (default, Mar 27 2019, 13:36:35) 
[GCC 9.0.1 20190227 (Red Hat 9.0.1-0.8)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```
 * `>>>` is known as python prompt.
 * Use `CTRL + d` to exit from the terminal or `exit()` command.
 * After quitting, all programs will get destroyed.
 
## My first program
* `print()` method is used to display output like `printf` in *C language*.

```
>>> print('Welcome to FOSSMEET, PUNE')
Welcome to FOSSMEET, PUNE
```

* We can also print in multiple lines by using `\n`.
```
>>> print('Welcome to FOSSMEET, PUNE\n Let\'s Learn Python 3')
Welcome to FOSSMEET, PUNE
 Let's Learn Python 3
```
We can `\` to escape any characters.

## [Use *#* to comment the code](https://www.python.org/dev/peps/pep-0008/#comments)
Anything written after `#` will be ignored.
```
>>> # print('This is a comment')
... 
>>> 
``` 

## Variables
* Variables in Python allows us to store information and give it a label.
  We can use to retrieve that information later.

* We can store numbers, strings (*a sequence of characters*) and complex data
  types.

* We assign values to variables by putting the value to the right of an equal
  sign.

* Python is a [General purpose programming language](https://en.wikipedia.org/wiki/General-purpose_programming_language).

* Let's define a variable.
```
>>> a = 12 # *a* is a variable holding the value 2
>>> b = 'Hello' # *b* is another variable holding string
>>> a
12
>>> b
'Hello'
>>> 
```
* Variable can be called any times based on needs.

## [String representation](https://docs.python.org/3/tutorial/introduction.html#strings)
* We can represent string using single, double or triple quotes.
```
>>> a = 'Hello World'
>>> a
'Hello World'
>>> b = "It is a double quote string"
>>> b
'It is a double quote string'
>>> c = """
... It is a multi line string
... Have fun, when we print it
... """
>>> c
'\nIt is a multi line string\nHave fun, when we print it\n'
>>> print(c)

It is a multi line string
Have fun, when we print it
>>> 
```
* We can `print` method to display the output.

## [Whitespaces and Indentation](https://docs.python.org/2.0/ref/indentation.html)
* We give whitespaces between operators to make the code more readable.
* Space at the beginning of a line is known as indentation.
* On using the wrong indentation, it will give indentation error
* Let's see
```
>>> a = 'foobar'

>>>  a = 'foobar'
  File "<stdin>", line 1
    a = 'foobar'
    ^
IndentationError: unexpected indent
>>> 
```

## Variable Naming
* Name of the variable should be meaningful.
* We generally use Number, Characters and underscore for naming
  variables.
* On using special characters it will through error.
```
>>> foobar = 'first string'
>>> foo_bar = 'second string'
>>> foo12 = 'Great'
>>> $foo12 = 'test'
  File "<stdin>", line 1
    $foo12 = 'test'
    ^
SyntaxError: invalid syntax
```
* Python provides a list of `keywords` which can't be used a variable name.

## Multiple assignment in a single line
We can even assign multiple values in a single line.
```
>>> a, b, c = 'Hello', 2, 'bar'
>>> a
'Hello'
>>> b
2
>>> c
'bar'
>>>
``` 

## Using Python as a calculator
```
>>> 100 + 200
300
>>> 100 - 300
-200
>>> 10 * 20 + 30
230
>>> (10 * 20 / 2 -100 ) + 50 
50.0
>>> 2 ** 4
16
>>> 8 / 5
1.6
>>> 8 // 5
1
>>> (10 * 20 / 2 -100 ) + 50 # We can call it as a expression
50.0
```
* `+`, `-`, `*`, `/` are used for addition, substraction, multiplication and
  division.
* `**` for calculating powers.
* `/` returns floating point numbers.
* `//` is used to discard fractional part.
* We can also try `BODMAS` rule in an expression.
* These are known as arithmetic operators.

## Relational Operators
```
>>> 1 < 2 # Is less than
True
>>> 3 > 34 # Is greater than
False
>>> 23 == 45 # Is equal to
False
>>> 1 >= 2 # Greater than or equal ot
False
>>> 2 <= 3 # Lesss than or equal to
True
>>> 10 != 20 # Not equal to
True
```

## Logical Operator
* `and` and `or` are a logical operator.
* `x and y` returns `False` if `x` is `False` else it returns evaluation of `y`.
  If `x` is `True`, it returns `True`.
```
>>> 1 and 4
4
>>> 1 or 4
1
>>> -1 or 4
-1
>>> 0 or 4
4
>>> 0 and 4
0
```

## Shorthand Operator
* `x operator = expression` is the syntax for shorthand operators.
```
>>> a = 15
>>> b = 2
>>> b += 30   # Same as b = b + 30
>>> b
32
```

## Taking input from keyword
* `input()` method is used to take `input` from `keyboard`.
 ```
 >>> input("Enter your name: ")
Enter your name: Chandan Kumar
'Chandan Kumar'
>>> myname = input("Enter your name: ")
Enter your name: raukadah
>>> myname
'raukadah'
>>> 
 ```
## Type conversion
* We can use `type()` to check the data type of a variable.
* We can also convert it.
```
>>> a = 10
>>> c = 1.5
>>> type(a)
<class 'int'>
>>> type(b)
<class 'str'>
>>> type(c)
<class 'float'>
>>> # let's convert a into float
... 
>>> float(a)
10.0
>>> int(b)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: invalid literal for int() with base 10: 'hello'
>>> # string cannot be converted into int or float
... 
>>> int(c)
1
>>> str(c)
'1.5'
```

## String Concatenation
* Same type of string literals can be joined
* if the variable is not same type then convert it by using `+`
```
>>> a = 'hello'
>>> b = 'COEP'
>>> a + b
'helloCOEP'
>>> c = 10
>>> a + c
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: cannot concatenate 'str' and 'int' objects
>>> a + str(c) # use str() method to convert from int to string then add
'hello10'
```

## Writing a program in file
* All Python programs are written with `.py` extension.
* Create a file named `first_program.py` and write the following code.
```
#!/usr/bin/env python3

myname = input("Enter your name: ")
print('Welcome to Python3 Fun Class %s' % myname)
```
* Make the program executable.
```
$ chomd +x first_program.py
```
* Then run it.
```
$./first_program.py
```
* On the first line you can `#!`, what we call it [sha-bang](https://en.wikipedia.org/wiki/Shebang_\(Unix\)).
  The `sha-bang` indicates that the Python interpreter should run this code.

## Decision Making using if, else
While working on programs, we always encounter with making decisions.
Based on the condition, we need to perform tasks or do other tasks.
We can use `if` keyword to that.
```
if expression:
    do
```
```
if expression:
    do
elif expression:
    then do
else:
    do something else
```
It works only when expression is `True` otherwise it goes to next line.
```
>>> a = 100
>>> if a % 2 == 0:
...     print('Even Number')
... else:
...     print('Odd Number')
... 
Even Number
>>> 
```
### Truth value testing
```
>>> a = True
>>> if a:
...     print("a is True")
a is True
```

## Functions
* When we have to do a certain set of operation multiple times and reuse it
  with in codebase then we need to define a function.
* `def` keyword is used to define a function.
* Syntax:
```
def function_name(function_arguments):
    do some stuff
    return something
```
* Here function_arguments are not mandatory.
* function arguments can be passed in any fashion
* If return is not define, it will `None`.
```
>>> def sum(a, b):
...     print(a + b)
... 
>>> sum(2,3)
5
>>> sum(a=2, b=3)
5
>>> return_value = sum(1, 2)
3
>>> print(return_value)
None
>>> def sum(a, b):
...     return a + b
... 
>>> result = sum(1, 2)
>>> result
3
>>> print(result)
3
```

## Passing controls using loops
### While loop
```
>>> a, b = 0, 1
>>> while b < 100:
...     print(a, end=',')
...     a, b = b, a+b
... 
0,1,1,2,3,5,8,13,21,34,55,>
```

### For loop
In Python loop works over a `Iterator` object,
might be a `list`, `string`, `tuples`, `dictionary`, `set` etc.
```
for i in sequence: 
    do some stuff
```
Let's `print` the letter of a word.
```
>>> word = "fossmeet"
>>> for i in word:
...     print(i, end='*')
... 
f*o*s*s*m*e*e*t*
```

### Looping over integers
* Use `range()` function.
* `range()` can be used in three ways.
* `range(n)`: will contain numbers form `0` through `n-1`
* `range(x, y)`: will start from `x` and end at `y-1`
* `range(x, y, z)`: will start at `x` and continue as `x+z`, `x+2z` until `x+kz` is less than `y`.
```
>>> range(10)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
>>> range(5, 10)
[5, 6, 7, 8, 9]
>>> range(0, 10, 3)
[0, 3, 6, 9]
>>> range(-10, -100, -30)
[-10, -40, -70]
>>> for i in range(10):
...     print('{0} square is {1}'.format(i, i ** 2))
... 
0 square is 0
1 square is 1
2 square is 4
3 square is 9
4 square is 16
5 square is 25
6 square is 36
7 square is 49
8 square is 64
9 square is 81
```
