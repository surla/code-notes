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

**Floats**
Any number with a decimal point is called a *float*

**Integers and Floats**
Dividing any two numbers always results in a float. Even whole number answers.

**Underscores in Numbers**
In Python 3.6 and later you may use underscoes to make large numbers more readable. 

```python
population = 10_000_000_000
```

