## **Set Methods**

### **1. `add(x)`**
Adds an element to the set.
```python
s = {1, 2, 3}
s.add(4)
print(s)  # Output: {1, 2, 3, 4}
```

### **2. `remove(x)`**
Removes an element from the set; raises an error if the element is not found.
```python
s = {1, 2, 3}
s.remove(2)
print(s)  # Output: {1, 3}
```

### **3. `discard(x)`**
Removes an element without raising an error if not found.
```python
s = {1, 2, 3}
s.discard(2)
print(s)  # Output: {1, 3}
```

### **4. `pop()`**
Removes and returns a random element.
```python
s = {1, 2, 3}
print(s.pop())  # Output: 1 (random)
print(s)  # Remaining elements
```

### **5. `clear()`**
Removes all elements from the set.
```python
s = {1, 2, 3}
s.clear()
print(s)  # Output: set()
```

### **6. `union(set2)`**
Returns a new set containing all elements from both sets.
```python
s1 = {1, 2, 3}
s2 = {3, 4, 5}
print(s1.union(s2))  # Output: {1, 2, 3, 4, 5}
```

### **7. `intersection(set2)`**
Returns a set containing common elements.
```python
s1 = {1, 2, 3}
s2 = {2, 3, 4}
print(s1.intersection(s2))  # Output: {2, 3}
```

### **8. `difference(set2)`**
Returns elements only in the first set.
```python
s1 = {1, 2, 3}
s2 = {2, 3, 4}
print(s1.difference(s2))  # Output: {1}
```

### **9. `symmetric_difference(set2)`**
Returns elements that are in either set, but not both.
```python
s1 = {1, 2, 3}
s2 = {2, 3, 4}
print(s1.symmetric_difference(s2))  # Output: {1, 4}
```

---

This document provides a complete reference for working with tuples and sets in Python. 🚀
