

| Component | Description |
|-----------|-------------|
| `lambda` | Keyword indicating a lambda function |
| `arguments` | Comma-separated input parameters |
| `expression` | Single expression to evaluate and return |

---

## Basic Examples

### Regular Function vs Lambda
```python
# Regular function
def square(x):
    return x * x

# Lambda function
square_lambda = lambda x: x * x

print(square(5))        # Output: 25
print(square_lambda(5)) # Output: 25
```

### Multiple Arguments
```python
# Regular function
def add(a, b):
    return a + b

# Lambda with multiple arguments
add_lambda = lambda a, b: a + b

print(add(5, 3))        # Output: 8
print(add_lambda(5, 3)) # Output: 8
```

### No Arguments
```python
# Lambda with no arguments
greet = lambda: "Hello, World!"
print(greet())  # Output: Hello, World!
```
