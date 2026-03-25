

```markdown
# Python Function Arguments

## Overview

Arguments are values passed to a function during a call. Python supports multiple types of arguments, giving you flexibility in how you pass data to functions.

---

## 1. Default Arguments

Default arguments assume a default value if no value is provided in the function call.

### Syntax:
```python
def function_name(param=default_value):
    # function body
```

### Example:
```python
def greet(name, message="Hello"):
    """Greets a user with optional custom message"""
    print(f"{message}, {name}!")

# Using default message
greet("Alice")                    # Output: Hello, Alice!

# Overriding default message
greet("Bob", "Good morning")      # Output: Good morning, Bob!
```

### Important Rules:
- Default arguments must come **after** non-default arguments
- Default values are evaluated only once (at function definition)

```python
# ✅ Correct
def func(a, b=10, c=20):
    pass

# ❌ Incorrect (syntax error)
def func(a=10, b):
    pass
```


