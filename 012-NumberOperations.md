# Python Numbers Guide

## Introduction
Python provides multiple numerical data types, each designed for different use cases. This guide covers integers, floating-point numbers, complex numbers, and other advanced numerical representations.

---

## **1. Integer (`int`)**
### **Features:**
- Whole numbers (positive, negative, or zero)
- No decimal points
- Arbitrary precision (limited by memory)

### **Operations:**
```python
x = 100
y = -50

# Arithmetic Operations
print(x + y)  # Addition: 50
print(x - y)  # Subtraction: 150
print(x * 2)  # Multiplication: 200
print(x // 3) # Floor Division: 33
print(x % 3)  # Modulus: 1
print(x ** 2) # Exponentiation: 10000

# Type Checking
print(isinstance(x, int))  # True
```

---

## **2. Floating Point (`float`)**
### **Features:**
- Numbers with decimal points
- Supports scientific notation (`1.2e3` = `1200`)
- Precision limited by machine’s floating-point representation (IEEE 754)

### **Operations:**
```python
a = 3.14
b = -0.0001

# Arithmetic Operations
print(a + b)   # Addition: 3.1399
print(a - b)   # Subtraction: 3.1401
print(a * 2)   # Multiplication: 6.28
print(a / 2)   # Division: 1.57
print(a ** b)  # Exponentiation

# Type Checking
print(isinstance(a, float))  # True
```

---

## **3. Complex Numbers (`complex`)**
### **Features:**
- Includes a real part and an imaginary part (`j` instead of `i` in mathematics)
- Built-in support in Python (`a + bj`)

### **Operations:**
```python
c1 = 2 + 3j
c2 = 1 - 2j

# Arithmetic Operations
print(c1 + c2)  # (3+1j)
print(c1 - c2)  # (1+5j)
print(c1 * c2)  # (8+1j)
print(c1 / c2)  # (-0.8+1.4j)

# Type Checking
print(isinstance(c1, complex))  # True
```

---

## **4. Boolean (`bool`) - Subtype of `int`**
### **Features:**
- Two values: `True` (1) and `False` (0)
- Can be used in arithmetic operations

### **Operations:**
```python
t = True
f = False

print(t + f)  # 1 (True is 1, False is 0)
print(t * 5)  # 5
print(f - 3)  # -3
print(bool(0), bool(1), bool(-2))  # False, True, True
```

---

## **5. Decimal (`decimal.Decimal`) - High-Precision Float**
### **Operations:**
```python
from decimal import Decimal

d1 = Decimal('0.1')
d2 = Decimal('0.2')

print(d1 + d2)  # 0.3 (Exact precision)
print(d1 * d2)  # 0.02
print(d1 / d2)  # 0.5
```

---

## **6. Fraction (`fractions.Fraction`)**
### **Operations:**
```python
from fractions import Fraction

frac1 = Fraction(1, 3)
frac2 = Fraction(2, 5)

print(frac1 + frac2)  # 11/15
print(frac1 - frac2)  # 1/15
print(frac1 * frac2)  # 2/15
print(frac1 / frac2)  # 5/6
```

---

## **7. Binary, Octal, Hexadecimal Representations**
### **Operations:**
```python
binary_num = 0b1010
octal_num = 0o12
hex_num = 0xA

print(bin(binary_num))  # '0b1010'
print(oct(octal_num))   # '0o12'
print(hex(hex_num))     # '0xa'
```

---

## **8. Converting Between Number Types**
### **Operations:**
```python
x = 10
print(float(x))  # Convert int to float: 10.0

y = 3.99
print(int(y))  # Convert float to int: 3 (Truncation)

print(complex(x))  # Convert int to complex: (10+0j)
print(Fraction(y))  # Convert float to fraction: 399/100

print(bin(x))  # '0b1010'
print(oct(x))  # '0o12'
print(hex(x))  # '0xa'
```

---

## **9. Mathematical Operations (`math` Module)**
```python
import math

print(math.sqrt(16))    # Square root: 4.0
print(math.factorial(5))  # Factorial: 120
print(math.gcd(24, 36))   # GCD: 12
print(math.sin(math.pi/2))  # 1.0
print(math.log(100, 10))    # Logarithm base 10: 2.0
print(math.exp(2))  # e^2
print(math.ceil(3.4))  # Ceiling function: 4
print(math.floor(3.9))  # Floor function: 3
```

---

## **Conclusion**
Python provides a variety of number types to handle different mathematical needs efficiently. Whether you're working with simple arithmetic, scientific computations, or high-precision calculations, Python has a suitable data type for you.

---

### *Happy Coding! 🚀*

