---

## 3. Positional Arguments

Positional arguments are passed in the **exact order** of parameters defined in the function.

### Example:
```python
def introduce(name, age, city):
    print(f"I'm {name}, {age} years old, from {city}")

# Order matters!
introduce("Alice", 25, "New York")     # ✅ Correct
introduce(25, "Alice", "New York")     # ❌ Wrong order
```

### Output:
```
I'm Alice, 25 years old, from New York
I'm 25, Alice years old, from New York  # Incorrect interpretation
```

---

