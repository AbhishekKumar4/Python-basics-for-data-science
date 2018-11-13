# Variables

- Named location used to store data in the memory.
- Each variable must have a unique name called identifier.
- In Python we don't assign values to the variables, whereas Python gives the reference of the object (value) to the variable.
- In Python, variables do not need declaration to reserve memory space. The "variable declaration" or "variable initialization" happens automatically when we assign a value to a variable.
- Use the assignment operator = to assign the value to a variable.
- *Python is a type inferred language, it can automatically infer (know) Apple.com is a String and declare website as a String.*


# Constants

- A constant is a type of variable whose value cannot be changed.
- All in capital letters and underscores separating the words.(Just like java)
- In reality, we don't use constants in Python. The globals or constants module(module means a new file containing variables, functions etc which is imported to main file.) is used throughout the Python programs.


# Rules and Naming convention for variables and constants

- Use camelCase notation to declare a variable. It starts with lowercase letter.
- Use capital letters where possible to declare a constant.
- Never use special symbols like !, @, #, $, %, etc.
- Don't start name with a digit.
- Constants are put into Python modules and meant not be changed.
- Constant and variable names should have combination of letters in lowercase (a to z) or uppercase (A to Z) or digits (0 to 9) or an underscore (_).


# Literals

- Literal is a raw data given in a variable or constant.

**Numeric Literals**
Example : 
- a = 0b1010 #Binary Literals
- b = 100 #Decimal Literal 
- c = 0o310 #Octal Literal
- d = 0x12c #Hexadecimal Literal

**String literals**

A string literal is a sequence of characters surrounded by quotes. We can use both single, double or triple quotes for a string. And, a character literal is a single character surrounded by single or double quotes.

Example : 
- strings = "This is Python"
- char = "C"
- multiline_str = """This is a multiline string with more than one line code."""
- unicode = u"\u00dcnic\u00f6de"
- raw_str = r"raw \n string"

**Boolean literals**

A Boolean literal can have any of the two values: True or False.

Example: 
- x = (1 == True)
- y = (1 == False)
- a = True + 4
- b = False + 10

**Special literals**

Python contains one special literal i.e. None. We use it to specify to that field that is not created.

Example : 
- food = None

**Literal Collections**

There are four different literal collections List literals, Tuple literals, Dict literals, and Set literals.

Example : 
- fruits = ["apple", "mango", "orange"] #list
- numbers = (1, 2, 3) #tuple
- alphabets = {'a':'apple', 'b':'ball', 'c':'cat'} #dictionary
- vowels = {'a', 'e', 'i' , 'o', 'u'} #set
