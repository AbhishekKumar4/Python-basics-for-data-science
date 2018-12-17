# Data Types

- Every value in Python has a datatype.
- Since everything is an object in Python programming, data types are actually classes and variables are instance (object) of these classes.
- In Python, we don’t need to declare a variable with explicitly mentioning the data type. This feature is famously known as dynamic typing.
- Python determines the type of a literal directly from the syntax at runtime. For example – the quotes mark the declaration of a string value, square brackets represent a list and curly brackets for a dictionary.

# Python data types
 - Booleans
 - Numbers
 - Strings
 - Bytes
 - Lists
 - Tuples
 - Sets
 - Dictionaries
 
 # Booleans
  - Boolean in Python can have two values – True or False.
  - In some cases, the boolean constants “True” and “False” might also act as numbers.
  
  ```
  >>> A, B = True + 0, False + 0
  >>> print(A, B)
  1 0
  ```
  
  - It is evident from the above example that True is 1 and the value of False is 0. And they will turn into numbers during arithmetic operations.
  
  # Numbers
  
  - Integers, floating point numbers and complex numbers falls under Python numbers category. They are defined as int, float and complex class in Python.
  - Unlike many languages which have only integers and floats, Python introduces complex as a new type of numbers.
  - Python has a built-in function type() to determine the data type of a variable or the value.
  - Another built-in function isinstance() is there for testing the type of an object.
  - In Python, we can add a “j” or “J” after a number to make it imaginary or complex.
  - Complex numbers are written in the form, x + yj, where x is the real part and y is the imaginary part.
  
  ```
  num = 7
  print("The number (", num, ") is of type", type(num))
  # Output : The number ( 7 ) is of type <class 'int'>
  
  num = 7.0
  print("The number (", num, ") is of type", type(num))
  # Output :The number ( 7.0 ) is of type <class 'float'>

  num = 2+7j
  print("The number ", num, " is of type", type(num))
  # Output : The number (2+7j) is of type <class 'complex'>
  
  print("The number ", num, " is complex number?", isinstance(2+7j, complex))
  # Output : The number (2+7j) is complex number? True
  ```
  
  - A floating point number is accurate up to 15 decimal places. Integer and floating points are separated by decimal points.
  ```
  >>> b = 0.1234567890123456789
  >>> print(b)
  0.12345678901234568
  # Notice that the float variable b got truncated.
  ```
  
  - To form a complex number, we can even use the type as a constructor. See the example below.
```
  >>> complex(1.2,5)
  (1.2+5j)
```
# Strings

- sequence of one or more characters enclosed within either single quotes ‘ or double quotes ”
- Python also supports multi-line strings which require a triple quotation mark at the start and one at the end.

```
>>> str = 'A string wrapped in single quotes'
>>> str
'A string wrapped in single quotes'
>>> str = "A string enclosed within double quotes"
>>> str
'A string enclosed within double quotes'
>>> str = """A multiline string
starts and ends with
a triple quotation mark."""
```
# Bytes

- The byte is an immutable type in Python. It can store a sequence of bytes (each 8-bits) ranging from 0 to 255.
- Similar to an array, we can fetch the value of a single byte by using the index. But we can not modify the value.

**Differences between a byte and the string**

  - Byte objects contain a sequence of bytes whereas the strings store sequence of characters.
  - The bytes are machine-readable objects whereas the strings are just in human-readable form.
  - Since the byte is machine-readable, so they can be directly stored to the disk. Whereas, the strings first need to encoded before       getting on to the disk.
  
# Lists

- Python list is an array like construct which stores arbitrarily typed objects in an ordered sequence. It is very flexible and does not have a fixed size. Index in a list begins with zero in Python.
- It is a heterogeneous collection of items of varied data types. For example, a list object can store the files in a folder, or the employee data in a company etc.

````
>>> this_is_list = [True, False, 1, 1.1, 1+2j, 'Learn', b'Python']
>>> first_element = this_is_list[0]
>>> print(first_element)
True

````

- List objects are mutable. Python allows modifying a list or its elements via assignments as well as through the built-in list methods.

````
>>> alist = ['This', 'is', 'list']
>>> id(alist)
56321160
>>> alist
['This', 'is', 'list']
>>> alist[2] = 'a list'
>>> id(alist)
56321160
>>> alist
['This', 'is', 'a list']
````

**Nested List**

- A list can contain another list. Such a list is called as the nested list.

````
>>> nested = [[1,1,1], [2,2,2], [3,3,3]]
>>> for items in nested:
	for item in items:
		print(item, end=' ')
		
1 1 1 2 2 2 3 3 3
````

**Slicing A List in python**

- The list is also one of the Python data types which supports slicing like we learned previously with Strings. With the slicing operator [ ], we can extract an element or a bunch of them from a list.

````
>>> languages = ['C', 'C++', 'Python', 'Java', 'Go', 'Angular']
>>> print('languages[0:3] = ', languages[0:3])
languages[0:3] =  ['C', 'C++', 'Python']
>>> print('languages[2:] = ', languages[2:])
languages[2:] =  ['Python', 'Java', 'Go', 'Angular']
````

# Tuples

A tuple is a heterogeneous collection of Python objects separated by commas. It means objects of different data types can co-exist in a tuple.

- Define a tuple using enclosing parentheses () having its elements separated by commas inside.

The tuple and a list are somewhat similar as they share the following traits.
  - Both objects are an ordered sequence.
  - They enable indexing and repetition.
  - Nesting is allowed.
  - They can store values of different types.
  
  ````
# tuple with nesting
first_tuple = (3, 5, 7, 9)
second_tuple = ('learn', 'python 3')
nested_tuple = (first_tuple, second_tuple)
print(nested_tuple)
# Output - ((3, 5, 7, 9), ('learn', 'python 3'))

  ````
  
  **Tuple Slicing**
````  
sample_tuple = (0 ,1, 2, 3, 4)

tuple_without_first_item = sample_tuple[1:]
print(tuple_without_first_item)

tuple_reverse = sample_tuple[::-1]
print(tuple_reverse)
````

**Tuple V/S List**

- Tuples do differ a bit from the list as they are immutable.
- Python does not allow to modify a tuple after it is created.
- We can not add or remove any element later. Instead, Python expects us to create a new one with the updated sequence of elements.

**Tuple with Mutable Objects As Elements**

Modifying a tuple is forbidden. But Python doesn’t enforce it on the elements. It means we can update them if they are mutable objects.

**Need of tuple**

- Python uses tuples to return multiple values from a function.
- Tuples are more lightweight than lists.
- It works as a single container to stuff multiple things.
- We can use them as a key in a dictionary.

#Set

Set is an unordered collection of unique items. Set is defined by values separated by comma inside braces { }. **Items in a set are not ordered.**

````
>>> a = {1,2,2,3,3,3}
>>> a
{1, 2, 3}
````

# Dictionary

- Dictionary is an unordered collection of key-value pairs (as in java).
- It is generally used when we have a huge amount of data. Dictionaries are optimized for retrieving data. We must know the key to retrieve the value.
- Dictionaries are defined within braces {} with each item being a pair in the form key:value. Key and value can be of any type.

