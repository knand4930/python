# Python Inheritance and `super()` Usage

Inheritance allows a class (child class) to acquire properties and behaviors (methods) from another class.

---

## **1. Single Inheritance**
A child class inherits from a single parent class.
```python
class Parent:
    def show(self):
        print("This is Parent class")

class Child(Parent):
    def display(self):
        print("This is Child class")

obj = Child()
obj.show()    # Inherited from Parent
obj.display() # Own method
```

---

## **2. Multiple Inheritance**
A child class inherits from multiple parent classes.
```python
class Parent1:
    def method1(self):
        print("Parent1 method")

class Parent2:
    def method2(self):
        print("Parent2 method")

class Child(Parent1, Parent2):
    def childMethod(self):
        print("Child method")

obj = Child()
obj.method1()
obj.method2()
obj.childMethod()
```

---

## **3. Multilevel Inheritance**
A class inherits from another child class.
```python
class Grandparent:
    def grandparent_method(self):
        print("Grandparent method")

class Parent(Grandparent):
    def parent_method(self):
        print("Parent method")

class Child(Parent):
    def child_method(self):
        print("Child method")

obj = Child()
obj.grandparent_method()
obj.parent_method()
obj.child_method()
```

---

## **4. Hierarchical Inheritance**
Multiple child classes inherit from the same parent class.
```python
class Parent:
    def parent_method(self):
        print("Parent method")

class Child1(Parent):
    def child1_method(self):
        print("Child1 method")

class Child2(Parent):
    def child2_method(self):
        print("Child2 method")

obj1 = Child1()
obj2 = Child2()

obj1.parent_method()
obj1.child1_method()

obj2.parent_method()
obj2.child2_method()
```

---

## **5. Hybrid Inheritance**
Combination of multiple types of inheritance.
```python
class Base:
    def base_method(self):
        print("Base method")

class A(Base):
    def method_a(self):
        print("A method")

class B(Base):
    def method_b(self):
        print("B method")

class C(A, B):
    def method_c(self):
        print("C method")

obj = C()
obj.base_method()
obj.method_a()
obj.method_b()
obj.method_c()
```

---

# **Using `super()` in Inheritance**

## **1. Calling Parent Class Method**
```python
class Parent:
    def show(self):
        print("This is Parent class")

class Child(Parent):
    def show(self):
        super().show()  # Calls Parent's show method
        print("This is Child class")

obj = Child()
obj.show()
```
**Output:**
```
This is Parent class
This is Child class
```

---

## **2. Using `super()` in Constructor (`__init__` method)**
```python
class Parent:
    def __init__(self, name):
        self.name = name
        print(f"Parent constructor called, Name: {self.name}")

class Child(Parent):
    def __init__(self, name, age):
        super().__init__(name)  # Calling Parent's constructor
        self.age = age
        print(f"Child constructor called, Age: {self.age}")

obj = Child("Alice", 25)
```
**Output:**
```
Parent constructor called, Name: Alice
Child constructor called, Age: 25
```

---

## **3. Calling Parent Class Methods in Multiple Inheritance**
```python
class A:
    def show(self):
        print("A's method")

class B(A):
    def show(self):
        super().show()  # Calls A's method
        print("B's method")

class C(B):
    def show(self):
        super().show()  # Calls B's method
        print("C's method")

obj = C()
obj.show()
```
**Output:**
```
A's method
B's method
C's method
```

---

## **4. Using `super()` in Hybrid Inheritance**
Helps in the **Method Resolution Order (MRO)**.
```python
class A:
    def show(self):
        print("A's method")

class B(A):
    def show(self):
        super().show()
        print("B's method")

class C(A):
    def show(self):
        super().show()
        print("C's method")

class D(B, C):  # Inheriting from B and C
    def show(self):
        super().show()  # Resolves method using MRO
        print("D's method")

obj = D()
obj.show()
```
**Output (MRO follows `B -> C -> A` order):**
```
A's method
C's method
B's method
D's method
```

---

## **Why Use `super()`?**
✅ **Avoids redundancy** – Calls the parent class method without explicitly naming it.  
✅ **Follows MRO** – Ensures the correct order of execution in multiple inheritance.  
✅ **Allows extendability** – Makes the code modular and easy to modify.

🚀 `super()` is a powerful tool in Python's inheritance system!
