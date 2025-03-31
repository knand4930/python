# Polymorphism in Python

Polymorphism in Python allows different classes to share the same method names but execute different behaviors. Below are different types of polymorphism with examples:

---

## 1. Method Overriding (Runtime Polymorphism)
- A child class provides a different implementation of a method inherited from a parent class.

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
```
### Output:
```
Dog barks
Cat meows
Animal makes a sound
```

---

## 2. Method Overloading (Simulated in Python)
- Achieved using default parameters or `*args` and `**kwargs`.

```python
class MathOperations:
    def add(self, a, b, c=0):
        return a + b + c

math_op = MathOperations()
print(math_op.add(2, 3))      # Output: 5
print(math_op.add(2, 3, 4))   # Output: 9
```

---

## 3. Operator Overloading
- Modifying the behavior of built-in operators using the `__add__`, `__sub__`, `__mul__`, etc.

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, other):
        return Point(self.x + other.x, self.y + other.y)

p1 = Point(1, 2)
p2 = Point(3, 4)
p3 = p1 + p2
print(p3.x, p3.y)  # Output: 4 6
```

---

## 4. Polymorphism with Functions
- Functions can accept different objects that share the same method name.

```python
class Car:
    def move(self):
        return "Car is moving"

class Boat:
    def move(self):
        return "Boat is sailing"

def transport_mode(vehicle):
    print(vehicle.move())

transport_mode(Car())  # Output: Car is moving
transport_mode(Boat())  # Output: Boat is sailing
```

---

## 5. Polymorphism with Inheritance
- Parent and child classes having the same method but with different behaviors.

```python
class Shape:
    def area(self):
        pass  # Placeholder

class Square(Shape):
    def __init__(self, side):
        self.side = side

    def area(self):
        return self.side * self.side

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

shapes = [Square(4), Circle(3)]
for shape in shapes:
    print(shape.area())
```
### Output:
```
16
28.26
```

---

These are the different ways polymorphism works in Python! 🚀

