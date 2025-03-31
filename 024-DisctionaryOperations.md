# Dictionary Methods in Python

Python provides several built-in methods to work with dictionaries. Below is a comprehensive list of dictionary methods with descriptions and examples.

---

## 1. `dict.clear()`
**Removes all items from the dictionary.**  
```python
my_dict = {"a": 1, "b": 2}
my_dict.clear()
print(my_dict)  # Output: {}
```

---

## 2. `dict.copy()`
**Returns a shallow copy of the dictionary.**  
```python
my_dict = {"a": 1, "b": 2}
copy_dict = my_dict.copy()
print(copy_dict)  # Output: {'a': 1, 'b': 2}
```

---

## 3. `dict.fromkeys(iterable, value)`
**Creates a dictionary with specified keys and a common value.**  
```python
keys = ["a", "b", "c"]
d = dict.fromkeys(keys, 0)
print(d)  # Output: {'a': 0, 'b': 0, 'c': 0}
```

---

## 4. `dict.get(key, default)`
**Returns the value for the given key, or a default if the key is missing.**  
```python
my_dict = {"a": 1, "b": 2}
print(my_dict.get("a"))  # Output: 1
print(my_dict.get("c", 0))  # Output: 0
```

---

## 5. `dict.items()`
**Returns a view object of dictionary’s key-value pairs.**  
```python
my_dict = {"a": 1, "b": 2}
print(list(my_dict.items()))  # Output: [('a', 1), ('b', 2)]
```

---

## 6. `dict.keys()`
**Returns a view object of all dictionary keys.**  
```python
my_dict = {"a": 1, "b": 2}
print(list(my_dict.keys()))  # Output: ['a', 'b']
```

---

## 7. `dict.values()`
**Returns a view object of all dictionary values.**  
```python
my_dict = {"a": 1, "b": 2}
print(list(my_dict.values()))  # Output: [1, 2]
```

---

## 8. `dict.pop(key, default)`
**Removes and returns the value for the given key, or a default if the key is missing.**  
```python
my_dict = {"a": 1, "b": 2}
print(my_dict.pop("a"))  # Output: 1
print(my_dict)  # Output: {'b': 2}
```

---

## 9. `dict.popitem()`
**Removes and returns the last inserted key-value pair as a tuple.**  
```python
my_dict = {"a": 1, "b": 2}
print(my_dict.popitem())  # Output: ('b', 2)
print(my_dict)  # Output: {'a': 1}
```

---

## 10. `dict.setdefault(key, default)`
**Returns the value of a key; if missing, inserts the key with the default value.**  
```python
my_dict = {"a": 1}
print(my_dict.setdefault("a", 100))  # Output: 1
print(my_dict.setdefault("b", 200))  # Output: 200
print(my_dict)  # Output: {'a': 1, 'b': 200}
```

---

## 11. `dict.update(other_dict)`
**Updates the dictionary with another dictionary or key-value pairs.**  
```python
my_dict = {"a": 1}
my_dict.update({"b": 2, "c": 3})
print(my_dict)  # Output: {'a': 1, 'b': 2, 'c': 3}
```

---

## 12. `dict.__contains__(key)`
**Checks if a key exists in the dictionary (same as `in` keyword).**  
```python
my_dict = {"a": 1, "b": 2}
print(my_dict.__contains__("a"))  # Output: True
print("a" in my_dict)  # Output: True (same result)
```

---

## 13. `dict.__delitem__(key)`
**Deletes an item by key (same as `del d[key]`).**  
```python
my_dict = {"a": 1, "b": 2}
del my_dict["a"]
print(my_dict)  # Output: {'b': 2}
```

---

## 14. `dict.__getitem__(key)`
**Gets the value of a key (same as `d[key]`).**  
```python
my_dict = {"a": 1, "b": 2}
print(my_dict.__getitem__("a"))  # Output: 1
```

---

## 15. `dict.__setitem__(key, value)`
**Sets a key-value pair (same as `d[key] = value`).**  
```python
my_dict = {}
my_dict.__setitem__("a", 100)
print(my_dict)  # Output: {'a': 100}
```

---

### 📌 **Conclusion**
This document covers all dictionary methods in Python with examples. Mastering these will help you efficiently work with dictionaries in Python. 🚀

