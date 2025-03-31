# Python Basics

## 1. Variables and Data Types
A variable stores data, and Python has various data types:

```python
x = 10         # Integer
y = 3.14       # Float
name = "John"  # String
is_valid = True  # Boolean
fruits = ["apple", "banana"]  # List
```

---

## 2. Operators

### **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`, `//`, `**`
```python
a = 10
b = 3
print(a + b)  # 13 (Addition)
print(a ** b) # 1000 (Exponentiation)
```

### **Logical Operators**: `and`, `or`, `not`
```python
x = True
y = False
print(x and y)  # False
print(x or y)   # True
```

### **Comparison Operators**: `==`, `!=`, `>`, `<`, `>=`, `<=`
```python
print(5 > 3)   # True
print(5 == 5)  # True
```

### **Bitwise Operators**: `&`, `|`, `^`, `~`, `<<`, `>>`
```python
a = 5  # 101 in binary
b = 3  # 011 in binary
print(a & b)  # 1 (Bitwise AND)
print(a | b)  # 7 (Bitwise OR)
```

---

## 3. Conditional Statements
```python
age = 18
if age >= 18:
    print("You are an adult")
elif age > 12:
    print("You are a teenager")
else:
    print("You are a child")
```

---

## 4. Loops

### **For Loop**
```python
for i in range(5):  
    print(i)  # 0 1 2 3 4
```

### **While Loop**
```python
x = 0
while x < 3:
    print(x)
    x += 1
```

---

## 5. Functions

### **Using `def`**
```python
def greet(name):
    return "Hello, " + name

print(greet("Alice"))
```

### **Lambda Function**
```python
square = lambda x: x * x
print(square(5))  # 25
```

---

## 6. Exception Handling
```python
try:
    num = int(input("Enter a number: "))
    print(10 / num)
except ZeroDivisionError:
    print("Cannot divide by zero")
except ValueError:
    print("Invalid input, enter a number")
finally:
    print("Execution completed")
```

These are the **basic concepts of Python** that help in writing efficient code! 🚀

