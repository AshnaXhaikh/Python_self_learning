### Using `global` for Global Variables

```python
global_var = 100

def outer():
    def inner():
        global global_var
        global_var += 1
        return global_var
    
    return inner

func = outer()
print(func())  # Output: 101
print(global_var)  # Output: 101
```

