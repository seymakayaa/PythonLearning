# Python Notes 

- For a comment placed on one line use ```#```, more than one line use ```""" """``` or ```''' '''```.

- We learn to data type of variable with ```type()``` function.

- String variables can be shown:
```
  ​	x = 'Alice' or x = "Alice"
```
- Variable names is case-sensitive. a and A are not the same.

- Variable names rules

   * must start with a letter or underscore character.
   * cannot start with a number.
   * can only contain alpha-numeric characters and underscores.
   * case-sensitive.
   * cannot be any of the python keywords.

- Camel Case : ```myVariableName```, Pascal Case: ```MyVariableName```, Snake Case: ```my_variable_name```

- Since Python does not have the concept of {}, indentation becomes crucial, and 4 spaces or 1 tab is used. For example:

```python
  ​if x > y:
  ​    print("hello")
```

-
```python
  x = "awesome"
  def myfunc():
      x = "fantastic"  # When we define a variable inside a function, it's only valid within that function and not outside it
      print("Python is " + x)
  myfunc()
  print("Python is " + x)
```

- global( ) function exp:
```python
  x = "awesome"
  def myfunc():
      global x   # When a variable is defined as global, its value becomes globally accepted, whether inside or outside the function.
      x = "fantastic"
  myfunc()
  print("Python is " + x)
```

- s = b'ankara' ---> Converts the variable to bytes.

- The expression "10+20" is ```death code```, don't impact anything in program.

- Compilers perform better code optimization than interpreters.

- print(r"kale\n")  r is regular. 
  ​	>>> kale\n
  
__Data Types__

  - ```Text Type:``` __str__ , x = "Hello"
  - ```Numeric Types:``` __int__, __float__, __complex__, x = 20(int), x = 20.5(float), x = 1j(complex)
  - ```Sequence Types:``` __list__, __tuple__, __range__, x = ["apple", "banana", "cherry"] list, x = ("apple",       "banana", "cherry") tuple, x = range(6) 
  - ```Mapping Types:``` __dict__,  x = {"name" : "John", "age" : 36}
  - ```Set Types:``` __set__, __frozenset__, x = {"apple", "banana", "cherry"} set, x = frozenset({"apple",           "banana", "cherry"}) frozen set
  - ```Boolean Type:``` __bool__,  x = True
  - ```Binary Types:``` __bytes__, __bytearray__, __memoryview__, x = b"Hello" bytes, x = bytearray(5), x =            memoryview(bytes(5))
  - ```None Type:``` __NoneType__, x = None
  
- Tuples are similar to lists but with one key difference: once a tuple is created, its elements cannot be modified, added, or removed. Each element within a tuple is referred to as an "__item__".
  
- Range type usually use 3 way:

1. One Parameter:

```python
for i in range(5):
	print(i)
```

2. Two Parameters:

```python
for i in range(2, 8):  #2 is start and 8 is stop
	print(i)
```

3. Three Parameters:

```python
for i in range(2, 10, 3):  #2 is start, 10 is stop, 3 is step
	print(i)
```

- Float can also be scientific numbers with an ```e/E``` to indicate the power of 10.
  
- Python does not have a random() function to make a random number, but Python has a built-in module called random that can be used to make random numbers.
  
- Multiline strings by using three double or single quotes.

- Get the charachter of a position n:
```python
  	x = "Hello world"
  		print(x[1])  # output:e
```

- Loop through the letters in the word:
  ```python
  	for x in "banana":
  		print(x)     
  ```

- To check if a certain phrase or character is present in a string, we can use the keyword ```in```.
  To check if a certain phrase or character is NOT present in a string, we can use the keyword ```not in```.


 ```python
	txt = "Hello World!"
	print("Hello" in txt)
```

- ```Slicing``` b = "Hello world!"
 	  b[2:5] --> llo ,
  	  b[:5]  --> Hello , 
  	  b[2:]  --> llo world! 

- ```upper() method```--> returns the string in upper case and ```lower() method```--> returns the string in lower case.
  ```python
  a = " string in upper"
  print(a.upper())  # output: STRING IN UPPER
  ```

- ```strip() method``` --> removes any whitespace from the beginning or the end.
- ```replace() method```--> replaces a string with another string.
- ```split() method```--> used to split the elements in a string. (list)
- ```format() method```--> demonstrates the usage of the format() method to fill a placeholder {} in a string with a specified value.
  ```python
  year = 21
  myAge = 8
  str = "it"
  txt = "This is the {2}st century. I will {0}. How is {1}?"
  print(txt.format(myAge,str,year))
  ```

```
__Method__	__Description__
capitalize()	Converts the first character to upper case
casefold()	Converts string into lower case
center()	Returns a centered string
count()	Returns the number of times a specified value occurs in a string
encode()	Returns an encoded version of the string
endswith()	Returns true if the string ends with the specified value
expandtabs()	Sets the tab size of the string
find()	Searches the string for a specified value and returns the position of where it was found
format()	Formats specified values in a string
format_map()	Formats specified values in a string
index()	Searches the string for a specified value and returns the position of where it was found
isalnum()	Returns True if all characters in the string are alphanumeric
isalpha()	Returns True if all characters in the string are in the alphabet
isascii()	Returns True if all characters in the string are ascii characters
isdecimal()	Returns True if all characters in the string are decimals
isdigit()	Returns True if all characters in the string are digits
isidentifier()	Returns True if the string is an identifier
islower()	Returns True if all characters in the string are lower case
isnumeric()	Returns True if all characters in the string are numeric
isprintable()	Returns True if all characters in the string are printable
isspace()	Returns True if all characters in the string are whitespaces
istitle()	Returns True if the string follows the rules of a title
isupper()	Returns True if all characters in the string are upper case
join()	Joins the elements of an iterable to the end of the string
ljust()	Returns a left justified version of the string
lower()	Converts a string into lower case
lstrip()	Returns a left trim version of the string
maketrans()	Returns a translation table to be used in translations
partition()	Returns a tuple where the string is parted into three parts
replace()	Returns a string where a specified value is replaced with a specified value
rfind()	Searches the string for a specified value and returns the last position of where it was found
rindex()	Searches the string for a specified value and returns the last position of where it was found
rjust()	Returns a right justified version of the string
rpartition()	Returns a tuple where the string is parted into three parts
rsplit()	Splits the string at the specified separator, and returns a list
rstrip()	Returns a right trim version of the string
split()	Splits the string at the specified separator, and returns a list
splitlines()	Splits the string at line breaks and returns a list
startswith()	Returns true if the string starts with the specified value
strip()	Returns a trimmed version of the string
swapcase()	Swaps cases, lower case becomes upper case and vice versa
title()	Converts the first character of each word to upper case
translate()	Returns a translated string
upper()	Converts a string into upper case
zfill()	Fills the string with a specified number of 0 values at the beginning
```


- Python Operators
	- ```Arithmetic operators``` (+, -, *, /, %, **, //)
	- ```Assignment operators``` (=, +=, -=, *=, /=, %=,**=, //=, &=, |=, ^=, >>=, <<=)
	- ```Comparison operators``` (==, !=, <=, >=, <, >)
	- ```Logical operators``` (and, or, not)
	- ```Identity operators``` (is, is not)
	- ```Membership operators``` (in, not in)
	- ```Bitwise operators``` (&, |, ^, ~, >>, <<)
 - To insert a new list item, without replacing any of the existing values, we can use the ```insert() method```.
   ```python
   thislist = ["apple", "banana", "cherry"]
   thislist.insert(2, "watermelon")
   print(thislist)
   ```

- To add an item to the end of the list, use the ```append() method```.
- To append elements from another list to the current list, use the ```extend() method```.
- The ```remove() method``` removes the specified item.
- The ```pop() method``` removes the specified index. If you do not specify the index, the pop() method removes the last item.
- The del keyword also removes the specified index.
  ```python
  thislist = ["apple", "banana", "cherry"]
  del thislist[0]
  print(thislist)
  ```
- The clear() method empties the list.
- List objects have a ```sort() method``` that will sort the list alphanumerically.
- Lists cannot be directly copied using list2 = list1. The ```copy() method``` or ```list()``` are used for copying.
  ```python
  thislist = ["a", "b", "c"]
  mylist = thislist.copy() # or mylist = list(thislist)
  print(mylist) 



__Summary List Methods__
1. ```append()``` --> Adds an element at the end of the list
2. ```clear()``` --> Removes all the elements from the list
3. ```copy()``` --> Returns a copy of the list
4. ```count()``` --> Returns the number of elements with the specified value
5. ```extend()``` --> Add the elements of a list (or any iterable), to the end of the current list
6. ```index()``` --> Returns the index of the first element with the specified value
7. ```insert()``` --> Adds an element at the specified position
8. ```pop()``` -->Removes the element at the specified position
9. ```remove()``` --> Removes the item with the specified value
10. ```reverse()``` --> Reverses the order of the list
11. ```sort()``` --> Sorts the list

