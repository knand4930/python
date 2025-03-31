# Object-Oriented Programming (OOP) in Python

Object-Oriented Programming (OOP) is a programming paradigm that structures code using objects and classes. It makes code **modular, reusable, and maintainable** by following key principles such as **Classes and Objects, Constructors, Inheritance, Polymorphism, Encapsulation, Abstraction, Magic Methods, Method Overloading, and the `super` Keyword**.

## 1. Classes and Objects

A **class** is a blueprint for creating objects, and an **object** is an instance of a class. Objects have attributes (data) and methods (functions).

### Example:
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def introduce(self):
        return f"Hi, I'm {self.name} and I'm {self.age} years old."

person = Person("Alice", 30)
print(person.introduce())  # Output: Hi, I'm Alice and I'm 30 years old.
```
✅ **Benefits:**
- Groups related data and behavior together.
- Enables object-oriented organization.

---

## 2. Constructors (`__init__`)

A **constructor** is a special method (`__init__`) that initializes object attributes when an instance of the class is created.

### Example:
```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def details(self):
        return f"Brand: {self.brand}, Model: {self.model}"

car = Car("Toyota", "Corolla")
print(car.details())  # Output: Brand: Toyota, Model: Corolla
```
✅ **Benefits:**
- Ensures objects are initialized properly.
- Eliminates manual attribute assignment.

---

## 3. Inheritance - Enabling Code Reuse

Inheritance allows a child class to **reuse properties and methods** from a parent class, reducing code duplication.

### Example:
```python
class Vehicle:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def details(self):
        return f"Brand: {self.brand}, Model: {self.model}"

class Car(Vehicle):  # Inheriting from Vehicle
    def __init__(self, brand, model, fuel_type):
        super().__init__(brand, model)
        self.fuel_type = fuel_type

    def details(self):
        return f"{super().details()}, Fuel Type: {self.fuel_type}"

car = Car("Toyota", "Corolla", "Petrol")
print(car.details())  # Output: Brand: Toyota, Model: Corolla, Fuel Type: Petrol
```
✅ **Benefits:**
- Avoids redundant code.
- Creates a hierarchical structure for better organization.

---

## 4. Polymorphism - Enabling Flexible Code

Polymorphism allows different classes to use the same method name but provide their own implementation.

### Example:
```python
class Animal:
    def speak(self):
        return "Animal makes a sound"

class Dog(Animal):
    def speak(self):
        return "Dog barks"

class Cat(Animal):
    def speak(self):
        return "Cat meows"

animals = [Dog(), Cat(), Animal()]
for animal in animals:
    print(animal.speak())

# Output:
# Dog barks
# Cat meows
# Animal makes a sound
```
✅ **Benefits:**
- Reduces conditional checks.
- Allows dynamic method overriding.

---

## 5. Encapsulation - Ensuring Data Security

Encapsulation restricts direct access to class attributes, ensuring data protection.

### Example:
```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private variable

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

    def get_balance(self):
        return self.__balance  # Controlled access

account = BankAccount(1000)
account.deposit(500)
print(account.get_balance())  # Output: 1500
```
✅ **Benefits:**
- Prevents unauthorized access.
- Ensures controlled data modification.

---

## 6. Abstraction - Hiding Implementation Details

Abstraction hides complex implementation logic and only exposes necessary functionalities.

### Example:
```python
from abc import ABC, abstractmethod

class Payment(ABC):  # Abstract Class
    @abstractmethod
    def process_payment(self, amount):
        pass

class CreditCardPayment(Payment):
    def process_payment(self, amount):
        return f"Paid {amount} via Credit Card"

class PayPalPayment(Payment):
    def process_payment(self, amount):
        return f"Paid {amount} via PayPal"

payment1 = CreditCardPayment()
payment2 = PayPalPayment()
print(payment1.process_payment(200))  # Output: Paid 200 via Credit Card
print(payment2.process_payment(300))  # Output: Paid 300 via PayPal
```
✅ **Benefits:**
- Hides unnecessary details.
- Enforces a consistent interface for subclasses.

---

## 7. Method Overloading - Multiple Behaviors for the Same Method

Method Overloading allows a class to define multiple versions of the same method, differing in the number or type of arguments.

### Example:
```python
class MathOperations:
    def add(self, a, b, c=0):  # Default argument for method overloading
        return a + b + c

math_op = MathOperations()
print(math_op.add(2, 3))      # Output: 5
print(math_op.add(2, 3, 4))   # Output: 9
```
✅ **Benefits:**
- Provides flexibility to use a method with different argument types.
- Reduces redundancy in method names.

---

## 8. The `super` Keyword - Accessing Parent Class Methods

The `super` keyword allows a child class to call a method from its parent class.

### Example:
```python
class Parent:
    def show(self):
        return "This is the parent class"

class Child(Parent):
    def show(self):
        return super().show() + " and this is the child class"

child = Child()
print(child.show())  # Output: This is the parent class and this is the child class
```
✅ **Benefits:**
- Helps in calling parent class methods.
- Avoids code duplication in child classes.

---

## Summary
| OOP Concept       | Description | Benefits |
|------------------|--------------------------------|---------------------------------|
| **Classes & Objects** | Blueprint for creating instances | Groups related data & methods |
| **Constructors**  | Initializes objects | Ensures proper attribute setup |
| **Inheritance**  | Reuse code from parent class | Avoids duplication |
| **Polymorphism** | Different classes, same method name | Makes code flexible |
| **Encapsulation** | Restrict direct access to attributes | Ensures data security |
| **Abstraction**  | Hide implementation details | Simplifies complexity |
| **Method Overloading** | Same method, different arguments | Provides flexibility |
| **`super` Keyword** | Access parent class methods | Reduces redundancy |

By combining these principles, OOP ensures a **structured, maintainable, and secure** approach to programming in Python.

---

### 🚀 Happy Coding!

