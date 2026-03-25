## Function Documentation (Docstring)

A **docstring** is a string literal that describes what a function does. It's placed immediately after the function definition.

### Example:
```python
def calculate_area(length, width):
    """
    Calculate the area of a rectangle.
    
    Parameters:
    length (float): The length of the rectangle
    width (float): The width of the rectangle
    
    Returns:
    float: The area of the rectangle
    """
    return length * width

# Access docstring
print(calculate_area.__doc__)
help(calculate_area)
```

---

## Best Practices

1. **Use descriptive function names** (verb + noun): `calculate_total()`, `get_user_data()`
2. **Keep functions small and focused** (Single Responsibility Principle)
3. **Add docstrings** to explain purpose and parameters
4. **Use meaningful parameter names**
5. **Return values instead of printing** inside functions (for reusability)

---

## Common Mistakes to Avoid

```python
# ❌ Bad: Function does too many things
def process_data(data):
    cleaned = clean(data)
    analyzed = analyze(cleaned)
    visualized = visualize(analyzed)
    return visualized

# ✅ Good: Separate functions for each task
def clean_data(data): ...
def analyze_data(data): ...
def visualize_data(data): ...

# ❌ Bad: Modifying global variables
total = 0
def add_to_total(x):
    global total
    total += x

# ✅ Good: Return value and assign
def add(x, y):
    return x + y
result = add(5, 3)
```

---

## Summary

| Concept | Description |
|---------|-------------|
| `def` | Keyword to define a function |
| Parameters | Input values to the function |
| Return | Output value from the function |
| Docstring | Documentation for the function |
| Function Call | Executing the function with `name()` |

```
