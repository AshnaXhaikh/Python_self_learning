### 3. **Factory Functions**
Create customized functions based on input parameters.

```python
def power_factory(exponent):
    """Create power functions dynamically"""
    
    def power(base):
        return base ** exponent
    
    return power

square = power_factory(2)
cube = power_factory(3)

print(square(4))   # Output: 16
print(cube(4))     # Output: 64
```

---
