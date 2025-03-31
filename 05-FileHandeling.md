# File Handling in Python

## 1. Reading and Writing Files (`open()`, `with` statement)
Python provides the `open()` function to read and write files efficiently. The `with` statement ensures proper resource management.

### Example:
```python
# Writing to a file
with open("sample.txt", "w") as file:
    file.write("Hello, World!")

# Reading from a file
with open("sample.txt", "r") as file:
    content = file.read()
    print(content)  # Output: Hello, World!
```

---

## 2. Working with CSV Files
Python’s `csv` module helps in handling CSV (Comma-Separated Values) files.

### Example:
```python
import csv

# Writing to a CSV file
with open("data.csv", "w", newline="") as file:
    writer = csv.writer(file)
    writer.writerow(["Name", "Age"])
    writer.writerow(["Alice", 25])

# Reading from a CSV file
with open("data.csv", "r") as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```

---

## 3. JSON and XML Parsing
Python supports JSON (`json` module) and XML (`xml.etree.ElementTree` module) parsing.

### JSON Example:
```python
import json

# Writing JSON
data = {"name": "Alice", "age": 25}
with open("data.json", "w") as file:
    json.dump(data, file)

# Reading JSON
with open("data.json", "r") as file:
    data = json.load(file)
    print(data)  # Output: {'name': 'Alice', 'age': 25}
```

### XML Example:
```python
import xml.etree.ElementTree as ET

# Parsing XML
xml_data = """<person><name>Alice</name><age>25</age></person>"""
root = ET.fromstring(xml_data)
print(root.find("name").text)  # Output: Alice
```

