
### 2. **Closures**
Inner functions can "remember" variables from outer scope even after outer function completes.

```python
def multiplier(factor):
    """Creates a function that multiplies by given factor"""
    
    def multiply(number):
        return number * factor
    
    return multiply

# Create specialized functions
double = multiplier(2)
triple = multiplier(3)

print(double(5))   # Output: 10
print(triple(5))   # Output: 15
```

