---

## What is Exception Handling?
Exception handling allows programs to handle errors gracefully without crashing. Instead of terminating abruptly, you can detect problems, respond to them, and continue execution.

---

## Basic Syntax
```python
try:
    # Risky code that might cause error
except SomeException:
    # Handle the error
else:
    # Runs only if no exception occurred
finally:
    # Always runs (cleanup code)
```

---

## Simple Example
```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Can't divide by zero!")

# Output: Can't divide by zero!
```

---

## Errors vs Exceptions

| **Error** | **Exception** |
|-----------|---------------|
| Serious problems, cannot be handled | Runtime problems, can be handled |
| Examples: SyntaxError, MemoryError | Examples: ZeroDivisionError, ValueError |
| Program cannot recover | Program can recover gracefully |

---

## The Four Keywords

| Keyword | Purpose |
|---------|---------|
| `try` | Contains code that might raise an exception |
| `except` | Catches and handles specific exceptions |
| `else` | Runs only if try block succeeds (no exceptions) |
| `finally` | Always runs (cleanup, closing files) |

---

## Catching Exceptions

### 1. **Catching Specific Exceptions**
```python
try:
    num = int("abc")
except ValueError:
    print("Invalid number!")
except ZeroDivisionError:
    print("Cannot divide by zero!")

# Output: Invalid number!
```

### 2. **Catching Multiple Exceptions**
```python
try:
    result = int("abc") / 0
except (ValueError, ZeroDivisionError) as e:
    print(f"Error: {e}")

# Output: Error: invalid literal for int() with base 10: 'abc'
```

### 3. **Catch-All Handler** (Use Carefully!)
```python
try:
    result = "100" / 20
except:
    print("Something went wrong!")  # Hides actual error type

# Output: Something went wrong!
```
⚠️ **Risk**: Hides debugging information. Use sparingly!

---

## Raising Exceptions

### Raise Built-in Exceptions
```python
def set_age(age):
    if age < 0:
        raise ValueError("Age cannot be negative")
    print(f"Age: {age}")

try:
    set_age(-5)
except ValueError as e:
    print(e)  # Output: Age cannot be negative
```

### Create Custom Exceptions
```python
class AgeError(Exception):
    pass

def set_age(age):
    if age < 0:
        raise AgeError("Age cannot be negative")
    print(f"Age: {age}")

try:
    set_age(-5)
except AgeError as e:
    print(e)  # Output: Age cannot be negative
```

---

## Complete Example with try-except-else-finally
```python
try:
    num = int(input("Enter a number: "))
    result = 100 / num
    
except ValueError:
    print("That's not a valid number!")
    
except ZeroDivisionError:
    print("Cannot divide by zero!")
    
else:
    print(f"Result is: {result}")  # Runs only if no exception
    
finally:
    print("Program execution complete")  # Always runs
```

---

## Advantages ✅
- **Improved reliability**: Program doesn't crash on unexpected input
- **Separation of concerns**: Error handling separate from business logic
- **Cleaner code**: Fewer conditional checks scattered throughout
- **Better debugging**: Tracebacks show exactly where problems occur

## Disadvantages ❌
- **Performance overhead**: Exception handling is slower than condition checks
- **Added complexity**: Multiple exception types can complicate code
- **Security risks**: Poorly handled exceptions might leak sensitive information

---

## Best Practices

1. **Catch specific exceptions** instead of using bare `except:`
2. **Use `else`** for code that should run only when no exceptions occur
3. **Use `finally`** for cleanup operations (closing files, database connections)
4. **Raise exceptions** for invalid states instead of returning error codes
5. **Create custom exceptions** for application-specific errors
6. **Don't suppress exceptions** silently — log them or handle appropriately

---

## Quick Reference

| Scenario | Keyword to Use |
|----------|----------------|
| Risky code | `try` |
| Handle specific errors | `except` |
| Code after successful try | `else` |
| Always execute cleanup | `finally` |
| Trigger an exception | `raise` |

---

This covers the essential concepts of Python exception handling!
