

```markdown
# Return Statement & Pass by Reference

## The Return Statement

The `return` statement exits a function and optionally passes a value back to the caller.

### Syntax:
```python
return [expression]
```

### Key Points:
- If no expression is provided, returns `None`
- Can return any Python object (numbers, strings, lists, dictionaries, functions, etc.)
- Exits the function immediately
- Multiple return values are returned as a tuple

---

## Basic Return Examples

### Returning Single Values
```python
def square(x):
    return x ** 2

def is_even(x):
    return x % 2 == 0

def greet(name):
    return f"Hello, {name}!"

print(square(5))    # Output: 25
print(is_even(4))   # Output: True
print(greet("Alice"))  # Output: Hello, Alice!
```

### Returning Multiple Values
```python
def get_min_max(numbers):
    """Return both min and max of a list"""
    return min(numbers), max(numbers)

# Unpack the tuple
min_val, max_val = get_min_max([1, 5, 3, 9, 2])
print(f"Min: {min_val}, Max: {max_val}")  # Output: Min: 1, Max: 9

# Or capture as tuple
result = get_min_max([1, 5, 3, 9, 2])
print(result)  # Output: (1, 9)
```

### Returning Complex Data Types
```python
def create_person(name, age):
    """Return a dictionary representing a person"""
    return {
        'name': name,
        'age': age,
        'is_adult': age >= 18
    }

person = create_person("Alice", 25)
print(person)  # Output: {'name': 'Alice', 'age': 25, 'is_adult': True}
```

### Returning Functions
```python
def make_multiplier(factor):
    """Return a function that multiplies by factor"""
    def multiplier(x):
        return x * factor
    return multiplier

double = make_multiplier(2)
triple = make_multiplier(3)

print(double(5))   # Output: 10
print(triple(5))   # Output: 15
```


