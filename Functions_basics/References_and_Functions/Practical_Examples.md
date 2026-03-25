---

## Practical Examples

### Example 1: Bank Account (Mutable)
```python
def deposit(account, amount):
    """Modify account balance (mutable object)"""
    account['balance'] += amount
    return account

def withdraw(account, amount):
    """Modify account balance with validation"""
    if account['balance'] >= amount:
        account['balance'] -= amount
        return True
    return False

my_account = {'owner': 'Alice', 'balance': 1000}
deposit(my_account, 500)
print(my_account['balance'])  # Output: 1500

withdraw(my_account, 200)
print(my_account['balance'])  # Output: 1300
```

### Example 2: String Processing (Immutable)
```python
def add_greeting(name):
    """Returns new string (original unchanged)"""
    return f"Hello, {name}!"

original = "Alice"
modified = add_greeting(original)

print(original)  # Output: Alice (unchanged)
print(modified)  # Output: Hello, Alice!
```

---

## Mutability Quick Reference

| Type | Mutability | Function Modification |
|------|------------|----------------------|
| `int` | Immutable | ❌ No change |
| `float` | Immutable | ❌ No change |
| `str` | Immutable | ❌ No change |
| `tuple` | Immutable | ❌ No change |
| `list` | Mutable | ✅ Affects original |
| `dict` | Mutable | ✅ Affects original |
| `set` | Mutable | ✅ Affects original |

---

## Best Practices

1. **Return values** instead of modifying mutable objects when possible
2. **Document behavior** clearly (whether function modifies input)
3. **Create copies** if you need to preserve original data
4. **Use immutable types** when you don't want modifications
5. **Be consistent** with function design

---

## Summary

| Concept | Description |
|---------|-------------|
| `return` | Exits function and sends back value |
| `None` | Default return value |
| Pass by Reference | Python passes object references |
| Immutable | Cannot be changed (new object created) |
| Mutable | Can be changed in place |
| Copy | Create new object to avoid modifying original |


---
