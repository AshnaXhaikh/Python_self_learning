## The `return` Statement

The `return` statement exits a function and optionally returns a value.

### Key Points:
- If no `return` statement, function returns `None`
- `return` can return any data type
- Multiple values can be returned as a tuple

### Examples:
```python
# Returns a single value
def square(num):
    return num ** 2

# Returns multiple values (as tuple)
def get_min_max(numbers):
    return min(numbers), max(numbers)

# No return statement
def print_message():
    print("Hello")  # Returns None implicitly

# Using returned values
result = square(5)        # result = 25
min_val, max_val = get_min_max([1, 2, 3, 4, 5])  # min_val=1, max_val=5
```
