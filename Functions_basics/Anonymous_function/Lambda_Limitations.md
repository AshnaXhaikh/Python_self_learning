---

## Lambda Limitations

### ❌ Cannot contain statements
```python
# ❌ Invalid
lambda x: print(x) or return x

# ✅ Valid (expression only)
lambda x: x * 2
```

### ❌ Cannot have multiple expressions
```python
# ❌ Invalid
lambda x: x + 1; x * 2

# ✅ Valid (combine into single expression)
lambda x: (x + 1) * 2
```

### ❌ Cannot include assignments
```python
# ❌ Invalid
lambda x: y = x * 2; y

# ✅ Use alternative approach
def multiply_by_two(x):
    y = x * 2
    return y
```
