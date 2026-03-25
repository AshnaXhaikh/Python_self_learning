
### Using `nonlocal` to Modify Outer Variables

Use the `nonlocal` keyword to modify variables from the outer (non-global) scope.

```python
def counter():
    count = 0
    
    def increment():
        nonlocal count  # Use outer variable
        count += 1
        return count
    
    return increment

my_counter = counter()
print(my_counter())  # Output: 1
print(my_counter())  # Output: 2
print(my_counter())  # Output: 3
```
