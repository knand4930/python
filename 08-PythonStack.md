# Stack Operations Example

## Description
This is a simple implementation of stack operations in Python using a list without a class. The stack supports the following operations:

- **Push (`push(x)`)**: Inserts an element at the top (O(1) time complexity)
- **Pop (`pop()`)**: Removes and returns the top element (O(1) time complexity)
- **Peek (`peek()`)**: Returns the top element without removing it (O(1) time complexity)
- **isEmpty (`isEmpty()`)**: Checks if the stack is empty (O(1) time complexity)
- **isFull (`isFull()`)**: Checks if the stack is full (for fixed-size stacks) (O(1) time complexity)

## Implementation
```python
# Creating a stack using a list
stack = []
capacity = 5  # Define a fixed capacity (optional)

# Push operation (O(1))
def push(stack, x):
    if len(stack) >= capacity:
        print("Stack is full")
    else:
        stack.append(x)
        print(f"Pushed {x} onto the stack")

# Pop operation (O(1))
def pop(stack):
    if not stack:
        print("Stack is empty")
    else:
        print(f"Popped {stack.pop()} from the stack")

# Peek operation (O(1))
def peek(stack):
    if not stack:
        print("Stack is empty")
    else:
        print(f"Top element is {stack[-1]}")

# isEmpty operation (O(1))
def isEmpty(stack):
    print("Stack is empty" if not stack else "Stack is not empty")

# isFull operation (O(1))
def isFull(stack, capacity):
    print("Stack is full" if len(stack) >= capacity else "Stack is not full")

# Example usage
push(stack, 10)
push(stack, 20)
push(stack, 30)
push(stack, 40)
push(stack, 50)
push(stack, 60)  # This should print "Stack is full"
peek(stack)
pop(stack)
pop(stack)
isEmpty(stack)
isFull(stack, capacity)
```

## Usage
Run the script in a Python environment to test stack operations. Modify the `capacity` variable to change the maximum size of the stack.

## Complexity Analysis
| Operation   | Time Complexity | Space Complexity |
|------------|----------------|-----------------|
| push()     | O(1)           | O(1)            |
| pop()      | O(1)           | O(1)            |
| peek()     | O(1)           | O(1)            |
| isEmpty()  | O(1)           | O(1)            |
| isFull()   | O(1)           | O(1)            |

## License
This code is free to use and modify.
