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

### Lists

A *list* is a collection of items in a particular order. Since list contain more than one element, it is best to make the name of the list plural. Square brackets ([]) indicate a list and individual elements are separated by commas.

```python
colors = ['red', 'blue', 'green', 'white]
```

**Accessing Elements in a List**
Lists are ordered collections. To access an element in a list, write the name of the list followed by the *index* enclosed in square brackets. 
Index positions start at 0.

```python
colors[0] 
>> 'red'
```

To return the last item in the list:
```python
colors[-1]
```

**Changing, Adding, and Removing Elements**

**Modifying Elements in a list**
```python
colors[0] = 'purple'
```

**Adding Elements to a List**
To append a new element to the end of the list:
```python
colors.append('yellow')
```

**Inseting Elements into a List**
To add an element at any position in the list use:
```python
colors.insert(0, 'pink')
```

**Removing Element from a List**
```python
del colors[1]
```

**pop() method**
pop() method removes the last item in a list. This method return the removed element and you can assign this to a variable.
```python
last_color = colors.pop()
```

To remove an item from any position in a list by including the index inside the parentheses.
```python
first_color = colors.pop(0)

**Removing an Item by Value
```python
favorite_color = 'yellow'
colors.remove(favorite_color)
```

**Organizing a List**
sort() method permanently sorts the list. This cannot be reversed. The follow list will be sorted alphabetically.
```python
colors.sort()
```

**To reverse the alphabetical order, pass the argument *reverse-True***
```python
colors.sort(reverse=True)
```

**To temporarily sort list use the sorted() function.**
```python
sorted(colors)
```

**To reverse the order of a list:**
```python
colors.reverse()
```

**To find the length of a list:**
```python
len(colors)
```

**Looping through list**
```pythong
colors = ['red', 'white', 'blue', 'green']
for color in colors:
  print(color)
  ```

**Making Numerical Lists
```python
for value in range(1,5):
  print(value)
```

**list() function**
numbers = list(range(1,6))
```

**List Comprehensions**
A *list comprehension* allows you to generate a list in one line of code.
```python
squares = [value**2 for value in range(1,11)]
```








