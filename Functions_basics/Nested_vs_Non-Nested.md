---

## Comparison: Nested vs Non-Nested

```python
# Without nested functions (global helper)
def validate_email(email):
    # validation logic
    return True

def register_user(email):
    if validate_email(email):
        print("User registered")

# With nested functions (encapsulated)
def register_user(email):
    def validate_email(email):
        # validation logic
        return True
    
    if validate_email(email):
        print("User registered")

# validate_email() is not exposed globally
```

