# Encapsulation in Python

Encapsulation is one of the core principles of Object-Oriented Programming (OOP). It restricts direct access to an object's data and methods, allowing controlled access through methods (getters and setters).

## Encapsulation Operations in Python
Python provides three types of access specifiers:

1. **Public Members (`self.variable`)** – Accessible from anywhere.
2. **Protected Members (`self._variable`)** – Intended for internal use but still accessible.
3. **Private Members (`self.__variable`)** – Cannot be accessed directly outside the class.

## Example
```python
class Car:
    def __init__(self, brand, speed):
        self.brand = brand        # Public
        self._speed = speed       # Protected
        self.__price = 50000      # Private

    def get_price(self):  # Getter for private variable
        return self.__price

    def set_price(self, price):  # Setter for private variable
        if price > 0:
            self.__price = price
        else:
            print("Invalid price")

# Creating object
car = Car("Tesla", 200)

# Accessing public member
print(car.brand)  # Output: Tesla

# Accessing protected member (Not recommended)
print(car._speed)  # Output: 200

# Accessing private member (Will raise an AttributeError)
# print(car.__price)  # Uncommenting will raise an error

# Accessing private member using getter
print(car.get_price())  # Output: 50000

# Modifying private member using setter
car.set_price(60000)
print(car.get_price())  # Output: 60000
```

## Summary
- **Public members**: Accessible from anywhere.
- **Protected members**: Should be accessed within the class or subclass.
- **Private members**: Cannot be accessed directly outside the class but can be accessed via getters and setters.

Encapsulation ensures **data security** and **controlled access** to class attributes. 🚀

