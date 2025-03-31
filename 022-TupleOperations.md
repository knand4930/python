# Python List and Tuple Methods

This document provides a complete list of Python list and tuple methods with examples and descriptions.

---

## **1. List Methods**

### **1.1 `append(x)`**
Adds an item at the end of the list.
```python
lst = [1, 2, 3]
lst.append(4)
print(lst)  # Output: [1, 2, 3, 4]
```

### **1.2 `insert(i, x)`**
Inserts an item `x` at index `i`.
```python
lst = [1, 3, 4]
lst.insert(1, 2)
print(lst)  # Output: [1, 2, 3, 4]
```

### **1.3 `extend(iterable)`**
Adds multiple elements to the list.
```python
lst = [1, 2]
lst.extend([3, 4, 5])
print(lst)  # Output: [1, 2, 3, 4, 5]
```

---

## **2. Tuple Methods**

### **2.1 `count(x)`**
Returns the number of times `x` appears in the tuple.
```python
tup = (1, 2, 2, 3, 2)
print(tup.count(2))  # Output: 3
```

### **2.2 `index(x)`**
Returns the index of the first occurrence of `x`.
```python
tup = (10, 20, 30, 40)
print(tup.index(30))  # Output: 2
```

### **2.3 Tuple Packing and Unpacking**
Tuples allow packing multiple values and unpacking them into variables.
```python
tup = (1, 2, 3)
a, b, c = tup
print(a, b, c)  # Output: 1 2 3
```

### **2.4 `len()`**
Returns the number of elements in the tuple.
```python
tup = (1, 2, 3, 4)
print(len(tup))  # Output: 4
```

### **2.5 `min()` and `max()`**
Finds the smallest and largest element in a tuple.
```python
tup = (5, 2, 8, 1)
print(min(tup))  # Output: 1
print(max(tup))  # Output: 8
```

### **2.6 `sum()`**
Returns the sum of all elements in a tuple.
```python
tup = (1, 2, 3, 4)
print(sum(tup))  # Output: 10
```

### **2.7 `sorted()`**
Returns a sorted list from the tuple.
```python
tup = (5, 3, 8, 2)
sorted_tup = sorted(tup)
print(sorted_tup)  # Output: [2, 3, 5, 8]
```

### **2.8 `tuple()`**
Converts an iterable (list, string, etc.) into a tuple.
```python
lst = [1, 2, 3]
tup = tuple(lst)
print(tup)  # Output: (1, 2, 3)
```

### **2.9 `in` and `not in` Operators**
Checks if an element exists in a tuple.
```python
tup = (10, 20, 30, 40)
print(20 in tup)  # Output: True
print(50 not in tup)  # Output: True
```

### **2.10 Concatenation and Repetition**
Tuples support concatenation and repetition.
```python
tup1 = (1, 2, 3)
tup2 = (4, 5)
print(tup1 + tup2)  # Output: (1, 2, 3, 4, 5)
print(tup1 * 2)  # Output: (1, 2, 3, 1, 2, 3)
```

### **2.11 Slicing Tuples**
Tuples support slicing to extract elements.
```python
tup = (0, 1, 2, 3, 4, 5)
print(tup[1:4])  # Output: (1, 2, 3)
print(tup[:3])  # Output: (0, 1, 2)
print(tup[-3:])  # Output: (3, 4, 5)
```

---

This document provides a complete reference for working with lists and tuples in Python. 🚀
