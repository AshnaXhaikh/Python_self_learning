
### Example 3: Memoization (Caching)
```python
def memoize(func):
    """Cache function results for repeated calls"""
    cache = {}
    
    def wrapper(n):
        if n not in cache:
            print(f"Calculating {n}...")
            cache[n] = func(n)
        else:
            print(f"Retrieving {n} from cache...")
        return cache[n]
    
    return wrapper

@memoize
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

print(fibonacci(5))
# Output:
# Calculating 5...
# Calculating 4...
# Calculating 3...
# Calculating 2...
# Calculating 1...
# Calculating 0...
# 5

print(fibonacci(5))  # Retrieving 5 from cache...
# Output: 5
```

---



