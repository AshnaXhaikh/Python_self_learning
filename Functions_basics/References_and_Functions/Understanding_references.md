---

### Understanding References

```python
def demonstrate_references(lst):
    print(f"Inside function - initial: {id(lst)}")  # Same ID as original
    
    # This modifies the original object
    lst.append(4)
    
    # This creates a NEW list (new ID)
    lst = [10, 20, 30]
    print(f"Inside function - after reassignment: {id(lst)}")
    
    return lst

original = [1, 2, 3]
print(f"Original ID: {id(original)}")

result = demonstrate_references(original)
print(f"Original after function: {original}")  # [1, 2, 3, 4]
print(f"Returned list: {result}")              # [10, 20, 30]
```

---

## Avoiding Unintended Modifications

### Copying Before Modification
```python
def safe_modify(lst):
    """Create a copy to avoid modifying original"""
    new_list = lst.copy()  # Create a copy
    new_list.append(4)
    return new_list

original = [1, 2, 3]
result = safe_modify(original)

print(f"Original: {original}")  # [1, 2, 3] (unchanged)
print(f"Result: {result}")      # [1, 2, 3, 4]
```

### Using Tuple for Immutable Data
```python
def modify_immutable_tuple(t):
    # Create new tuple (immutable)
    return t + (4,)

original = (1, 2, 3)
result = modify_immutable_tuple(original)

print(f"Original: {original}")  # (1, 2, 3)
print(f"Result: {result}")      # (1, 2, 3, 4)
```

