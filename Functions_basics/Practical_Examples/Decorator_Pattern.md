

### Example 2: Decorator Pattern (Simple)
```python
def timer():
    """Create a function timer decorator"""
    import time
    
    def decorator(func):
        def wrapper(*args, **kwargs):
            start = time.time()
            result = func(*args, **kwargs)
            end = time.time()
            print(f"{func.__name__} took {end - start:.4f} seconds")
            return result
        return wrapper
    
    return decorator

# Usage
@timer()
def slow_function():
    import time
    time.sleep(1)
    return "Done"

slow_function()  # Output: slow_function took 1.0023 seconds
```

