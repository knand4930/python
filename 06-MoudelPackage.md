# Modules and Packages in Python

## Creating and Importing Modules
A **module** is a file containing Python code (functions, classes, or variables) that can be imported into other scripts. A **package** is a directory containing multiple modules, along with an `__init__.py` file.

### Creating a Module
Save the following code in a file named `mymodule.py`:

```python
# mymodule.py
def greet(name):
    return f"Hello, {name}!"
```

### Importing the Module
Use the following script to import and use the module:

```python
import mymodule

print(mymodule.greet("Alice"))  # Output: Hello, Alice!
```

---

## Standard Libraries in Python
Python has several built-in modules that simplify common tasks.

### os (Operating System Module)
Used for interacting with the operating system.

```python
import os

print(os.getcwd())  # Get current working directory
os.mkdir("new_folder")  # Create a new folder
```

### sys (System Module)
Provides access to system-specific parameters and functions.

```python
import sys

print(sys.version)  # Show Python version
print(sys.argv)  # List of command-line arguments
```

### math (Mathematical Functions)
Provides functions for mathematical operations.

```python
import math

print(math.sqrt(25))  # Output: 5.0
print(math.pi)  # Output: 3.141592653589793
```

### datetime (Date and Time Handling)
Used for manipulating dates and times.

```python
from datetime import datetime

now = datetime.now()
print(now.strftime("%Y-%m-%d %H:%M:%S"))  # Format current date and time
```

---

## Virtual Environments
Virtual environments allow Python projects to have isolated dependencies.

### Using `venv` (Built-in Virtual Environment Module)
- Create a virtual environment:
  ```sh
  python -m venv myenv
  ```
- Activate the virtual environment:
  - **Windows:** `myenv\Scripts\activate`
  - **Mac/Linux:** `source myenv/bin/activate`
- Install packages:
  ```sh
  pip install requests
  ```

### Using `pipenv` (Dependency Manager)
- Install `pipenv`:
  ```sh
  pip install pipenv
  ```
- Create a virtual environment and install dependencies:
  ```sh
  pipenv install requests
  ```
- Activate the environment:
  ```sh
  pipenv shell
  ```

---

Enjoy coding with Python! 🚀
