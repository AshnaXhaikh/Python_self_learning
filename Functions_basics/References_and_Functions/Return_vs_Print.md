---

## Return vs Print

```python
# ❌ Bad: Function prints instead of returning
def calculate_sum_bad(a, b):
    print(a + b)  # Prints but doesn't return

result = calculate_sum_bad(5, 3)
print(result)  # Output: None (function returns None)

# ✅ Good: Function returns the value
def calculate_sum_good(a, b):
    return a + b

result = calculate_sum_good(5, 3)
print(result)  # Output: 8
```

**Rule:** Functions should **return** values, not print them, unless the sole purpose is to display output.

---

## Early Return

Use `return` to exit a function early when conditions are met.

```python
def find_first_even(numbers):
    """Return first even number, or None if none found"""
    for num in numbers:
        if num % 2 == 0:
            return num  # Early exit
    return None  # No even numbers found

print(find_first_even([1, 3, 5, 4, 7]))   # Output: 4
print(find_first_even([1, 3, 5, 7]))      # Output: None
```

