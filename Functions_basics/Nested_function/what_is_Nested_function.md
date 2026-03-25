---
```markdown
# Nested Functions (Function within Functions)

## What are Nested Functions?

A **nested function** (or inner function) is a function defined inside another function. The inner function can access variables from the outer function's scope.

---

## Basic Example

```python
def outer_function():
    """Outer function containing an inner function"""
    message = "Hello from outer!"
    
    def inner_function():
        """Inner function accessing outer scope"""
        print(message)
    
    inner_function()

outer_function()
# Output: Hello from outer!
```
