
---

## Lambda in Data Structures

### In Lists
```python
# List of lambda functions
operations = [
    lambda x: x + 1,    # increment
    lambda x: x * 2,    # double
    lambda x: x ** 2    # square
]

value = 5
for op in operations:
    print(op(value))
# Output:
# 6
# 10
# 25
```

### In Dictionaries
```python
# Dictionary of operations
calculators = {
    'add': lambda a, b: a + b,
    'subtract': lambda a, b: a - b,
    'multiply': lambda a, b: a * b,
    'divide': lambda a, b: a / b
}

print(calculators['add'](10, 5))        # Output: 15
print(calculators['multiply'](10, 5))   # Output: 50
```

