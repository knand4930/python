# Python List Methods

This document provides a complete list of Python list methods with examples and short descriptions.

---

## **1. Adding Elements to a List**

| **Method** | **Description** | **Example** |
|------------|---------------|------------|
| `append(x)` | Adds an item at the end of the list. | ```python
lst = [1, 2, 3]
lst.append(4)
print(lst)  # [1, 2, 3, 4]
``` |
| `insert(i, x)` | Inserts an item `x` at index `i`. | ```python
lst = [1, 3, 4]
lst.insert(1, 2)
print(lst)  # [1, 2, 3, 4]
``` |
| `extend(iterable)` | Adds multiple elements to the list. | ```python
lst = [1, 2]
lst.extend([3, 4, 5])
print(lst)  # [1, 2, 3, 4, 5]
``` |

---

## **2. Removing Elements from a List**

| **Method** | **Description** | **Example** |
|------------|---------------|------------|
| `remove(x)` | Removes the first occurrence of `x`. | ```python
lst = [1, 2, 3, 2]
lst.remove(2)
print(lst)  # [1, 3, 2]
``` |
| `pop(i)` | Removes and returns the item at index `i` (default is last). | ```python
lst = [1, 2, 3]
x = lst.pop(1)
print(lst)  # [1, 3]
print(x)  # 2
``` |
| `clear()` | Removes all elements from the list. | ```python
lst = [1, 2, 3]
lst.clear()
print(lst)  # []
``` |

---

## **3. Searching and Counting in a List**

| **Method** | **Description** | **Example** |
|------------|---------------|------------|
| `index(x)` | Returns the index of the first occurrence of `x`. | ```python
lst = [10, 20, 30, 40]
print(lst.index(30))  # 2
``` |
| `count(x)` | Returns the number of times `x` appears. | ```python
lst = [1, 2, 2, 3, 2]
print(lst.count(2))  # 3
``` |

---

## **4. Sorting and Reversing a List**

| **Method** | **Description** | **Example** |
|------------|---------------|------------|
| `sort()` | Sorts the list in **ascending order**. | ```python
lst = [3, 1, 4, 2]
lst.sort()
print(lst)  # [1, 2, 3, 4]
``` |
| `sort(reverse=True)` | Sorts the list in **descending order**. | ```python
lst = [3, 1, 4, 2]
lst.sort(reverse=True)
print(lst)  # [4, 3, 2, 1]
``` |
| `reverse()` | Reverses the order of elements. | ```python
lst = [1, 2, 3]
lst.reverse()
print(lst)  # [3, 2, 1]
``` |
| `sorted(lst)` | Returns a **new sorted list** (original remains unchanged). | ```python
lst = [5, 2, 8, 1]
new_lst = sorted(lst)
print(new_lst)  # [1, 2, 5, 8]
print(lst)  # [5, 2, 8, 1]
``` |

---

## **5. Copying a List**

| **Method** | **Description** | **Example** |
|------------|---------------|------------|
| `copy()` | Returns a **shallow copy** of the list. | ```python
lst = [1, 2, 3]
new_lst = lst.copy()
print(new_lst)  # [1, 2, 3]
``` |

---

## **6. List Comprehension (Alternative for Creating Lists)**

List comprehension allows creating lists **efficiently**:

```python
# Creates a list of squares (0², 1², 2², ..., 4²)
lst = [x**2 for x in range(5)]
print(lst)  # [0, 1, 4, 9, 16]
```

---

This document provides a complete reference for working with lists in Python. 🚀
