# More Data Types

## String
* String is a sequence of characters.
* We have seen the string representation in previous chapter.
* Python provides lots of built in method associated with it.

### Side by side string literals
```
>>> a = 'foo' 'bar'
>>> a
'foobar'
>>> a = "foo"
>>> a * 5
'foofoofoofoofoo'
```

### Have fun with string associated methods
```
>>> s = "chandan kumar"
>>> s.title() # returns a title case
'Chandan Kumar'
>>> z = s.upper() # Converts it to upper case
>>> z
'CHANDAN KUMAR'
>>> z.lower() # converts to lower case
'chandan kumar'
>>> s = "I am A FunnY ProgRAmmER"
>>> s.swapcase() # converts it to swapcase
'i AM a fUNNy pROGraMMer'
>>> s = "chkumar246 Kumar"
>>> s.isalpha() # Check for alphabets
False
>>> y = "chkumar"
>>> y.isalpha()
True
>>> y = '1234'
>>> y.isdigit() # check all characters are digit or not
True
>>> s = "Chandan Kumar"
>>> s.istitle() # check for title
True
>>> s = "PUNE"
>>> s.isupper() # Check for all characters are in uppercase
True
>>> s = 'pune'
>>> s.islower() # Check for all characters are in lowercase
True
```

### Let's split and Join a string
```
>>> a = 'We are learning Python'
>>> a.split()
['We', 'are', 'learning', 'Python']
>>> a.split() # Split the string based on spaces
['We', 'are', 'learning', 'Python']
>>> a.split('a') # Split the string at character *a*
['We ', 're le', 'rning Python']
>>> data = a.split()
>>> data
['We', 'are', 'learning', 'Python']
>>> type(data)
<class 'list'>
>>> # split() method always returns a list
... 
>>> # A list can be joined by join method.
... 
>>> a
'We are learning Python'
>>> "**".join("We are learning".split())
'We**are**learning'
>>> 
```

### Strip some characters from a string
```
>>> a = "abc\n"
>>> a.strip() # It will remove new line 
'abc'
>>> b = "https://facebook.com"
>>> b.lstrip('https://') # strip from left side
'facebook.com'
>>> b.rstrip(".com") # strip from right side
'https://facebook'
>>> domain_name = b.lstrip('https://').rstrip('.com')
>>> domain_name
'facebook'
>>> 
```
### Some more functions with string
```
>>> b
'https://facebook.com'
>>> '.com' in b
True
>>> len(b)
20
```
### String Indexing
* First character of a string has index `0`.
* Negative indices start form `-1`, when counted from right.
```
>>> word = "Welcome to FOSS MEET"
>>> word[0]
'W'
>>> word[-1]
'T'
>>> word[5]
'm'
>>> word[-3]
'E'
```

### String Slicing
* `string[x:y]` returns the string starting from index `x` to `y-1`.
```
>>> word[2:8]
'lcome '
>>> word[8]
't'
```

### String are immutable
It means we cannot update the characters of a string.
```
>>> word[5] = 'b'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
```

## List
* Comma separated values between square brackets
* List can be sliced, indexed and concatenated
* Lists are mutable it means we can append and remove items from a list.
```
>>> a = [1,2,3,4,5,6]
>>> a[0]
1
>>> a[-1]
6
>>> a[6]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
>>> a.append(1000)
>>> a
[1, 2, 3, 4, 5, 6, 1000]
>>> a[6]
1000
>>> b = ['hello', 'foo', 'bar']
>>> a + b
[1, 2, 3, 4, 5, 6, 1000, 'hello', 'foo', 'bar']
>>> a.remove(5)
>>> a
[1, 2, 3, 4, 6, 1000]
>>> ## nesting list
... 
>>> a = [1, 2, 3]
>>> b = ['foo', 'bar']
>>> nested_list = [a, b]
>>> nested_list
[[1, 2, 3], ['foo', 'bar']]
>>> nested_list[0]
[1, 2, 3]
>>> nested_list[1][-1]
'bar'
>>> len(a)
3
>>> 1 in a
True
>>> a = ['foo', 'bar', 'alpha']
>>> del a[1]
>>> a
['foo', 'alpha']
>>> len(a)
2
>>> 'foo' in a
True
```

## List Comprehensions
List comprehensions provide a concise way to create lists. 
Each list comprehension consists of an expression followed by a for clause, 
then zero or more for or if clauses. The result will be a list resulting
from evaluating the expression in the context of the for and if clauses 
which follow it.
```
>>> square_of_10 = [i ** 2 for i in range(11)]
>>> square_of_10
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

## Tuples
* Items separated by comma in a closed bracket.
* These are immutable, it means we cannot append or remove data from it.
```
>>> a = (1,2,3,'hello')
>>> a
(1, 2, 3, 'hello')
>>> type(a)
<class 'tuple'>
>>> a[2]
3
>>> a[-1]
'hello'
>>> divmod(15,2)
(7, 1)
>>> x, y = divmod(15, 2)
>>> x
7
>>> y
1
>>> del a[1]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'tuple' object doesn't support item deletion
>>> a = (100)
>>> type(a)
<class 'int'>
>>> # to create a tuple with single item
... 
>>> a = (100,)
>>> type(a)
<class 'tuple'>
```

## Set
A list of items with no duplicates in curly braces.
```
>>> a = 'axbecjnn2226'
>>> set(a)
{'n', 'e', 'a', '6', 'x', 'b', 'j', '2', 'c'}
>>> 
```
* Define another set `b` and try out `a - b`, `a | b`, `a & b`, `a ^ b`
* We can also add and remove values from set
```
>>> c
{'n', 'e', 'a', '6', 'x', 'b', 'j', '2', 'c'}
>>> c.add('hello')
>>> c
{'n', 'e', 'a', 'hello', '6', 'x', 'b', 'j', '2', 'c'}
>>> c.pop()
'n'
```

## Dictionaries
* Unordered set of key: value pairs under `{}` braces.
* Keys are unique in nature.
* Dictionaries are mutable but keys must be of immutable type.
* By using particular key, we can access or update the value.
* Values can be of any data type.
```
>>> mydict = {'number': 1, 'letter': 'foobar', 'mytuple':(1,2,3), 'foobar': [1,2,3,4]}
>>> mydict
{'number': 1, 'letter': 'foobar', 'mytuple': (1, 2, 3), 'foobar': [1, 2, 3, 4]}
>>> mydict['letter']
'foobar'
>>> mydict['number'] = "It is really a number"
>>> mydict
{'number': 'It is really a number', 'letter': 'foobar', 'mytuple': (1, 2, 3), 'foobar': [1, 2, 3, 4]}
>>> 
```

### Methods associated with dictionaries
```
>>> mydict.keys()
dict_keys(['number', 'letter', 'mytuple', 'foobar'])
>>> mydict.values()
dict_values(['It is really a number', 'foobar', (1, 2, 3), [1, 2, 3, 4]])
>>> mydict.items()
dict_items([('number', 'It is really a number'), ('letter', 'foobar'), ('mytuple', (1, 2, 3)), ('foobar', [1, 2, 3, 4])])
>>> 'foobar' in mydict
True
>>> len(mydict)
4
```
We can always run a loop over list, string, tuple and dict:

### Fun time
* Create a dictionary which has keys like numbers, strings, tuples, list, set and dict and put some value.  
  Run a for loop and print their data types and their content.

* Checkout lambda and map function
