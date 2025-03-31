# Python Keywords with Examples

## Boolean & None
- **`True`**, **`False`**: Boolean values  
- **`None`**: Represents "no value"

```python
x = True
y = False
z = None
```

## Control Flow
- **`if`**, **`elif`**, **`else`**: Conditional statements  
- **`for`**, **`while`**: Loops  
- **`break`**: Exit loop  
- **`continue`**: Skip iteration  
- **`pass`**: Placeholder  

```python
if x:
    print("True")
elif y:
    print("False")
else:
    pass  # Placeholder

for i in range(5):
    if i == 2:
        continue  # Skip 2
    print(i)
    if i == 3:
        break  # Stop at 3
```

## Exception Handling
- **`try`**, **`except`**, **`finally`**: Handle errors  
- **`raise`**: Manually throw an error  

```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
finally:
    print("Cleanup")
```

## Functions & Classes
- **`def`**: Define a function  
- **`return`**: Return a value  
- **`lambda`**: Anonymous function  
- **`class`**: Define a class  

```python
def add(a, b):
    return a + b

double = lambda x: x * 2

class Person:
    def __init__(self, name):
        self.name = name
```

## Scope & Variables
- **`global`**: Use a global variable  
- **`nonlocal`**: Modify outer function variable  

```python
x = 10
def modify():
    global x
    x = 20  # Modify global variable

def outer():
    y = 5
    def inner():
        nonlocal y
        y = 10  # Modify outer variable
```

## Importing & Modules
- **`import`**, **`from`**, **`as`**: Import modules  

```python
import math
from math import sqrt as square_root

print(square_root(16))
```

## Logical Operators
- **`and`**, **`or`**, **`not`**: Logical operations  
- **`is`**, **`in`**: Comparisons  

```python
print(True and False)  # False
print(not False)  # True
print("a" in "apple")  # True
print(x is 20)  # True (after modify())
```

## Asynchronous Programming
- **`async`**, **`await`**: Asynchronous functions  

```python
import asyncio

async def fetch_data():
    await asyncio.sleep(1)
    return "Data received"

asyncio.run(fetch_data())
```

## Miscellaneous
- **`del`**: Delete a variable  
- **`with`**: Context management (e.g., files)  
- **`assert`**: Debugging checks  
- **`yield`**: Generator function  

```python
with open("file.txt", "w") as f:
    f.write("Hello")

def generator():
    yield 1
    yield 2

g = generator()
print(next(g))  # 1
```

---

This document covers all Python keywords with brief explanations and examples. 🚀
