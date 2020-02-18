# PYTHON

------



[TOC]

------



## Basics of the Basics

### Print Statements

#### Basic

```python
# end = added to end of print statement (default \n)
# sep = what separates the items in the statement (default ' ')
print('Hello', end='', sep='')
print("Hello World!")

print('Hello', 'World')
# Hello World\n
print('Hello', 'World', end='', sep='')
#HelloWorld

```

#### f-Strings

Python 3.6 feature that is the most readable way to format text currently. f-Strings are string literals that have an f at the beginning and curly braces containing expressions that will be replaced with their values. The expressions are evaluated at runtime and then formatted using the _format_ protocol. 

```python
name = "Eric"
age = 74
f"Hello, {name}. You are {age}." # You can also use a capital F
```

##### Function Calls

You can also do function calls using f-Strings:

```python
def to_lowercase(input):
    return input.lower()
name = "Eric Bachman"
f"{to_lowercase(name)} is funny."
# eric bachman is funny.
```

##### f-Strings with Objects

You can even use objects created from classes with f-strings. Imagine you had the following class:

```python
class Comedian:
    def __init__(self, first_name, last_name, age):
        self.first_name = first_name
        self.last_name = last_name
        self.age = age

    def __str__(self):
        return f"{self.first_name} {self.last_name} is {self.age}."

    def __repr__(self):
        return f"{self.first_name} {self.last_name} is {self.age}. Surprise!"
```

You can do this:

```python
new_comedian = Comedian("Eric", "Idle", "74")
f"{new_comedian}"
# Eric Idle is 74
```

------

### Commenting

```python
# This is a comment
# There is no such thing as multiline comments in python. Every line must be separated by a hashmark and a space. 
```

------

### Input

```python
myName = input()
```

------

### Data Types

| **Data Type**          | **Examples**                            |
| ---------------------- | --------------------------------------- |
| Integer                | -2, -1, 0, 1, 2, 3, 4, 5                |
| Floating-point numbers | -1.25, -1.0, --0.5, 0.0, 0.5, 1.0, 1.25 |
| Strings                | 'a', 'aa', 'aaa', 'Hello!', '11 cats'   |

------

### String Concatenation

| **Situation**         | **Example**                                | Output      |
| --------------------- | ------------------------------------------ | ----------- |
| String + String       | 'Hello' + ' World'                         | Hello World |
| String + (Not String) | 'Hello ' + 42                              | ERROR       |
| String * Integer      | 'Hello ' * 2 (String replication operator) | Hello Hello |
|                       |                                            |             |

------

### String Functions

```python
# To find the length of a string (returns integer):
myName = input()
length = len(myName)
```

------

### Casting

| **Situation**              | **Function** | **Example**   |
| -------------------------- | ------------ | ------------- |
| Int or Float **TO** String | str()        | str(29)       |
| String **TO** Int          | int()        | int('29')     |
| String **TO** Float        | float()      | float('10.5') |



------

### Math Operators

| **Operator** | **Operation**                       | **Example** | **Evaluates to...** |
| ------------ | ----------------------------------- | ----------- | ------------------- |
| **           | Exponent                            | 2 ** 3      | 8                   |
| %            | Modulus / remainder                 | 22 % 8      | 6                   |
| //           | Integer division / floored quotient | 22 // 8     | 2                   |
| /            | Division                            | 22 / 8      | 2.75                |
| *            | Multiplication                      | 3 * 5       | 15                  |
| -            | Subtraction                         | 2 - 2       | 0                   |
| +            | Addition                            | 2 + 2       | 4                   |

PEMDAS applies