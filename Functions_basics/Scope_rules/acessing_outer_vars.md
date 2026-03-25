---

## Scope Rules

### Accessing Outer Variables

Inner functions can **read** outer variables but cannot **assign** to them directly.

```python
def outer():
    x = 10
    
    def inner():
        # ✅ Can read outer variable
        print(x)  # Output: 10
        
        # ❌ Cannot reassign outer variable
        # x = 20  # This creates a LOCAL variable
    
    inner()
```
