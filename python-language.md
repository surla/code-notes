# Python Programming Language

### Variables
Variable are labels that are assigned to values.

```python
message = "Hello Python world!"
```

### Strings
A string is a series of characters. You can use single or double quotes around strings.

```python
"This is a string"
'This is also a string'
```

**String Methods**
.title()
.upper()
.lower()

**Using Variables in Strings**
Use f-strings to create strings that use information associated with variables.

```python
first_name = "ada"
last_name = "lovelace"
full_name = f"{first_name} {last_name}"
```

Python 3.5 or earlier uses format() method
```python
full_name = "{} {}".format(first_name, last_name)
```

**Adding Whitespace to Strings with Tabs or Newlines**

```python
print("\nPython")
print("\tPython")
```

**Stripping Whitespace**

```python
.rstrip()
.lstrip()
.strip()
```

### Numbers

**Integers**
Add (+)
Subtract (-)
Multiply (*)
Divide (/)
Exponent (**)

**Parentheses**
Use parentheses to modify the order of operations
```python
(2 + 3) * 4
```

**Floats**
Any number with a decimal point is called a *float*

**Integers and Floats**
Dividing any two numbers always results in a float. Even whole number answers.

**Underscores in Numbers**
In Python 3.6 and later you may use underscoes to make large numbers more readable. 

```python
population = 10_000_000_000
```

**Multiple Assignments
Assign values to more than one variable using a single line. Often used when initializing a set of numbers.
```python
x, y, z = 0, 0 ,0
```

**Constants
A *constant* is like a variable whose value stays the same throughout the life of a program. Use all capital letters to indicate a variable should be treated as a constant. Contants can never be changed.
```python
CONST_NAME = "5000"
```

**Comments**
A *comment* allows you to write notes within a program. A # indicates a comment. 
```python
# This is a comment.
```




