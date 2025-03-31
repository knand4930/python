# Advanced Python Concepts

## 1. Decorators and Generators

### **Decorators**
Decorators are functions that modify the behavior of another function without modifying its structure. They are commonly used for logging, authentication, and performance measurement.

#### **Example: A decorator for logging function calls**
```python
import time

def timing_decorator(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        print(f"Function '{func.__name__}' executed in {end_time - start_time:.4f} seconds")
        return result
    return wrapper

@timing_decorator
def slow_function():
    time.sleep(2)
    print("Function execution complete.")

slow_function()
```

### **Generators**
Generators are functions that return an iterator using the `yield` keyword instead of `return`, making them memory efficient.

#### **Example: A generator for generating Fibonacci numbers**
```python
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        yield a
        a, b = b, a + b

for num in fibonacci(5):
    print(num)
```

## 2. Multithreading and Multiprocessing

### **Multithreading**
Multithreading allows parallel execution of tasks using threads. However, Python's Global Interpreter Lock (GIL) prevents true parallel execution for CPU-bound tasks.

#### **Example: Running multiple tasks using `threading`**
```python
import threading
import time

def print_numbers():
    for i in range(5):
        print(i)
        time.sleep(1)

thread1 = threading.Thread(target=print_numbers)
thread2 = threading.Thread(target=print_numbers)

thread1.start()
thread2.start()

thread1.join()
thread2.join()
```

### **Multiprocessing**
Multiprocessing allows true parallel execution of tasks by creating separate processes, which can bypass the GIL.

#### **Example: Running multiple tasks using `multiprocessing`**
```python
import multiprocessing
import time

def print_numbers():
    for i in range(5):
        print(i)
        time.sleep(1)

process1 = multiprocessing.Process(target=print_numbers)
process2 = multiprocessing.Process(target=print_numbers)

process1.start()
process2.start()

process1.join()
process2.join()
```

## 3. Memory Management and Garbage Collection

Python has automatic memory management, utilizing **reference counting** and **garbage collection**.

### **Reference Counting**
Every object in Python has a reference count. When an object's reference count reaches zero, it is automatically deallocated.

#### **Example: Reference counting**
```python
import sys

a = [1, 2, 3]
print(sys.getrefcount(a))  # Reference count of `a`
b = a  # Another reference to `a`
print(sys.getrefcount(a))  # Increased reference count

del b  # Deleting reference
print(sys.getrefcount(a))  # Decreased reference count
```

### **Garbage Collection**
Python's garbage collector removes cyclic references.

#### **Example: Demonstrating garbage collection**
```python
import gc

class Node:
    def __init__(self):
        self.ref = None

node1 = Node()
node2 = Node()

node1.ref = node2  # Creating a cyclic reference
node2.ref = node1

del node1
del node2

gc.collect()  # Forces garbage collection
```

## 4. Metaclasses

Metaclasses are "classes of classes" that define how a class behaves. They allow modification of class creation.

#### **Example: Custom metaclass**
```python
class Meta(type):
    def __new__(cls, name, bases, dct):
        dct['greet'] = lambda self: f"Hello from {name}"
        return super().__new__(cls, name, bases, dct)

class MyClass(metaclass=Meta):
    pass

obj = MyClass()
print(obj.greet())  # Outputs: Hello from MyClass
```

---

These advanced Python features enhance performance, optimize memory, and provide powerful customization options. 🚀

