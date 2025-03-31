# Abstraction in Python

## Overview
Abstraction is an important concept in **Object-Oriented Programming (OOP)**. It allows us to hide implementation details and expose only the necessary functionalities.

In Python, abstraction is achieved using **abstract classes** and **abstract methods** via the `ABC` (Abstract Base Class) module.

## Abstraction in Python

### 1. Abstract Class
An **abstract class** is a class that contains one or more **abstract methods**. It cannot be instantiated directly.

### 2. Abstract Method
An **abstract method** is a method declared in an abstract class but does not have an implementation. The child class **must** override it.

## Example: Implementing Abstraction in Python

```python
from abc import ABC, abstractmethod

# Abstract class
class Shape(ABC):  
    @abstractmethod
    def area(self):
        """Abstract method to calculate area"""
        pass
    
    @abstractmethod
    def perimeter(self):
        """Abstract method to calculate perimeter"""
        pass

# Concrete class implementing the abstract class
class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height
    
    def perimeter(self):
        return 2 * (self.width + self.height)

# Creating an object of Rectangle
rect = Rectangle(10, 5)
print("Area:", rect.area())          # Output: Area: 50
print("Perimeter:", rect.perimeter()) # Output: Perimeter: 30
```

## Key Points
- **Abstract classes cannot be instantiated directly.**
- **Abstract methods must be implemented in child classes.**
- **Abstraction helps in achieving data hiding and enforcing method implementation in subclasses.**

---

## Benefits of Abstraction
✅ Reduces code complexity by hiding implementation details.
✅ Enforces a contract for subclasses to implement necessary methods.
✅ Makes the code easier to maintain and extend.

Would you like more details or another example? 😊

