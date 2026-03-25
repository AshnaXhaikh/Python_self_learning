---

## Performance Considerations

Lambda functions are **not** inherently faster than regular functions. Use them for:
- **Readability** when logic is simple
- **Convenience** with functional programming tools
- **Brevity** in short, throwaway operations

```python
# Regular function (more readable for complex logic)
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

# Lambda (less readable for complex logic)
is_prime_lambda = lambda n: n > 1 and all(n % i != 0 for i in range(2, int(n**0.5) + 1))
```

---

## Summary

| Feature | Regular Function | Lambda Function |
|---------|-----------------|-----------------|
| Syntax | `def name():` | `lambda:` |
| Name | Has a name | Anonymous |
| Body | Multiple statements | Single expression |
| Return | Explicit `return` | Implicit |
| Use Case | Complex, reusable | Simple, one-time |
| Docstring | Yes | No |
```

