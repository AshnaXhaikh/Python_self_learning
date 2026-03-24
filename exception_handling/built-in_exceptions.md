Here are examples for the **most important** Python built-in exceptions:

---

## 1. **ZeroDivisionError**
```python
try:
    result = 10 / 0
except ZeroDivisionError as e:
    print(e)  # Output: division by zero
```

---

## 2. **TypeError**
```python
try:
    result = "hello" + 5
except TypeError as e:
    print(e)  # Output: can only concatenate str (not "int") to str
```

---

## 3. **ValueError**
```python
try:
    num = int("abc")
except ValueError as e:
    print(e)  # Output: invalid literal for int() with base 10: 'abc'
```

---

## 4. **IndexError**
```python
my_list = [1, 2, 3]
try:
    element = my_list[5]
except IndexError as e:
    print(e)  # Output: list index out of range
```

---

## 5. **KeyError**
```python
d = {"name": "Alice"}
try:
    value = d["age"]
except KeyError as e:
    print(e)  # Output: 'age'
```

---

## 6. **NameError**
```python
try:
    print(undefined_variable)
except NameError as e:
    print(e)  # Output: name 'undefined_variable' is not defined
```

---

## 7. **AttributeError**
```python
class MyClass:
    pass

obj = MyClass()
try:
    obj.some_attribute
except AttributeError as e:
    print(e)  # Output: 'MyClass' object has no attribute 'some_attribute'
```

---

## 8. **FileNotFoundError**
```python
try:
    with open("nonexistent.txt", "r") as file:
        content = file.read()
except FileNotFoundError as e:
    print(e)  # Output: [Errno 2] No such file or directory: 'nonexistent.txt'
```

---

## 9. **AssertionError**
```python
try:
    assert 1 == 2, "Numbers are not equal"
except AssertionError as e:
    print(e)  # Output: Numbers are not equal
```

---

## 10. **ImportError / ModuleNotFoundError**
```python
try:
    import nonexistent_module
except ModuleNotFoundError as e:
    print(e)  # Output: No module named 'nonexistent_module'
```

---

## 11. **KeyboardInterrupt**
```python
try:
    while True:
        pass  # Press Ctrl+C to interrupt
except KeyboardInterrupt:
    print("Program interrupted by user")
```

---

## 12. **RecursionError**
```python
def recursive_func():
    return recursive_func()  # Infinite recursion

try:
    recursive_func()
except RecursionError as e:
    print(e)  # Output: maximum recursion depth exceeded
```

---

## 13. **MemoryError**
```python
try:
    huge_list = [1] * (10**10)  # May cause MemoryError
except MemoryError as e:
    print("Memory limit exceeded")
```

---

## 14. **OverflowError**
```python
import math
try:
    result = math.exp(1000)  # Extremely large number
except OverflowError as e:
    print(e)  # Output: math range error
```

---

## 15. **StopIteration**
```python
my_list = [1, 2, 3]
iterator = iter(my_list)

try:
    print(next(iterator))  # 1
    print(next(iterator))  # 2
    print(next(iterator))  # 3
    print(next(iterator))  # Raises StopIteration
except StopIteration as e:
    print("No more items")
```

---

## Quick Reference Table

| Exception | When It Occurs | Example |
|-----------|----------------|---------|
| `ZeroDivisionError` | Division by zero | `10 / 0` |
| `TypeError` | Wrong type operation | `"hello" + 5` |
| `ValueError` | Invalid value | `int("abc")` |
| `IndexError` | Invalid list index | `list[10]` |
| `KeyError` | Invalid dict key | `dict["missing"]` |
| `NameError` | Undefined variable | `print(unknown)` |
| `AttributeError` | Missing attribute | `obj.missing_attr` |
| `FileNotFoundError` | Missing file | `open("missing.txt")` |
| `AssertionError` | Assert fails | `assert 1 == 2` |
| `ModuleNotFoundError` | Missing module | `import missing` |
| `KeyboardInterrupt` | Ctrl+C pressed | User interrupt |
| `RecursionError` | Infinite recursion | Recursive call |
| `MemoryError` | Out of memory | Too large list |

---

These are the most commonly encountered exceptions you'll see in everyday Python programming!
