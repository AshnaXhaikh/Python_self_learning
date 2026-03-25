---

## 2. Keyword Arguments

Keyword arguments allow you to pass values by explicitly specifying parameter names. **Order doesn't matter.**

### Example:
```python
def student_info(fname, lname, age):
    """Display student information"""
    print(f"Name: {fname} {lname}")
    print(f"Age: {age}")

# Positional arguments (order matters)
student_info("John", "Doe", 20)

# Keyword arguments (order doesn't matter)
student_info(lname="Smith", fname="Jane", age=22)
student_info(age=25, fname="Mike", lname="Brown")

# Mixing positional and keyword (positional must come first)
student_info("Sarah", age=24, lname="Wilson")
```

### Benefits:
- **Readability**: Code is self-documenting
- **Flexibility**: Order doesn't matter
- **Selective arguments**: Can skip some if they have defaults

