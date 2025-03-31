# Python String Operations

This document provides a comprehensive guide on **string operations in Python**, including **concatenation, slicing, length calculation, and more**.

---

## 1. String Concatenation Methods

### Using `+` Operator

```python
str1 = "Hello"
str2 = "World"
result = str1 + " " + str2  # "Hello World"
print(result)
```

### Using `join()`

```python
words = ["Hello", "World"]
result = " ".join(words)  # "Hello World"
print(result)
```

### Using f-strings

```python
name = "John"
greeting = f"Hello, {name}!"
print(greeting)  # "Hello, John!"
```

### Using `format()`

```python
name = "John"
greeting = "Hello, {}!".format(name)
print(greeting)  # "Hello, John!"
```

### Using `%` Formatting

```python
name = "John"
greeting = "Hello, %s!" % name
print(greeting)  # "Hello, John!"
```

---

## 2. String Slicing

Python allows slicing using the format:

```python
string[start:end:step]
```

### Examples:

```python
text = "Python Programming"

# Extract substring (index 0 to 5)
print(text[0:6])  # Output: "Python"

# Get last 5 characters
print(text[-5:])  # Output: "mming"

# Skip every second character
print(text[::2])  # Output: "Pto rgamn"

# Reverse the string
print(text[::-1])  # Output: "gnimmargorP nohtyP"
```

---

## 3. String Length

Use `len()` to get the number of characters in a string.

```python
text = "Hello, World!"
print(len(text))  # Output: 13
```

---

## 4. String Modification

### Convert to Uppercase and Lowercase

```python
text = "Hello, World!"
print(text.upper())  # "HELLO, WORLD!"
print(text.lower())  # "hello, world!"
```

### Capitalize First Letter

```python
print(text.capitalize())  # "Hello, world!"
```

### Title Case (First Letter of Each Word Capitalized)

```python
print(text.title())  # "Hello, World!"
```

### Swap Case (Upper → Lower and Lower → Upper)

```python
print(text.swapcase())  # "hELLO, wORLD!"
```

---

## 5. String Search & Replacement

### Finding Substrings

```python
text = "Python is awesome"
print(text.find("is"))  # Output: 7
print(text.index("is"))  # Output: 7
```

### Checking if a String Starts or Ends with a Substring

```python
print(text.startswith("Python"))  # True
print(text.endswith("awesome"))   # True
```

### Replacing Substrings

```python
new_text = text.replace("awesome", "great")
print(new_text)  # "Python is great"
```

---

## 6. String Splitting & Stripping

### Splitting a String

```python
text = "apple,banana,grape"
fruits = text.split(",")
print(fruits)  # ['apple', 'banana', 'grape']
```

### Removing Leading & Trailing Spaces

```python
text = "   Hello, World!   "
print(text.strip())  # "Hello, World!"
```

### Removing Only Leading or Trailing Spaces

```python
print(text.lstrip())  # "Hello, World!   "
print(text.rstrip())  # "   Hello, World!"
```

---

## 7. Checking String Properties

### Checking if String is Numeric

```python
text = "12345"
print(text.isdigit())  # True
```

### Checking if String is Alphabetic

```python
text = "Hello"
print(text.isalpha())  # True
```

### Checking if String is Alphanumeric

```python
text = "Hello123"
print(text.isalnum())  # True
```

### Checking if String is Lowercase or Uppercase

```python
text = "hello"
print(text.islower())  # True

text = "HELLO"
print(text.isupper())  # True
```

---

## 8. String Repetition

```python
text = "Hello "
print(text * 3)  # "Hello Hello Hello "
```

---

## 9. String Encoding & Decoding

### Encoding a String

```python
text = "Hello"
encoded_text = text.encode("utf-8")
print(encoded_text)  # b'Hello'
```

### Decoding a String

```python
decoded_text = encoded_text.decode("utf-8")
print(decoded_text)  # "Hello"
```

---

This covers almost all major string operations in Python. Let me know if you need more details! 🚀

