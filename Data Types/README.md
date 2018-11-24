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
