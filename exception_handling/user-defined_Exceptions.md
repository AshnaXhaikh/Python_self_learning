Here's a **summary of User-Defined Exceptions in Python**:

---

## What are User-Defined Exceptions?
Custom exceptions created by defining a new class that inherits from Python's built-in `Exception` class or its subclasses. They allow you to create application-specific error messages and handle unique error conditions.

---

## Steps to Create and Use User-Defined Exceptions

### 1. **Define the Exception Class**
```python
class InvalidAgeError(Exception):
    pass
```

### 2. **Raise the Exception**
```python
def set_age(age):
    if age < 0:
        raise InvalidAgeError("Age cannot be negative")
```

### 3. **Handle the Exception**
```python
try:
    set_age(-5)
except InvalidAgeError as e:
    print(e)
```

---

## Basic Example

```python
# Step 1: Define custom exception
class InvalidAgeError(Exception):
    def __init__(self, age, msg="Age must be between 0 and 120"):
        self.age = age
        self.msg = msg
        super().__init__(self.msg)
    
    def __str__(self):
        return f'{self.age} -> {self.msg}'

# Step 2: Use in code
def set_age(age):
    if age < 0 or age > 120:
        raise InvalidAgeError(age)
    print(f"Age set to: {age}")

# Step 3: Handle exception
try:
    set_age(150)
except InvalidAgeError as e:
    print(e)

# Output: 150 -> Age must be between 0 and 120
```

---

## Customizing Exception Classes

You can enhance custom exceptions with:
- **Additional attributes** (error codes, values)
- **Custom methods**
- **Overridden `__str__`** for better messages

### Example with Error Code
```python
class InvalidAgeError(Exception):
    def __init__(self, age, msg="Age must be between 0 and 120", error_code=1001):
        self.age = age
        self.msg = msg
        self.error_code = error_code
        super().__init__(self.msg)
    
    def __str__(self):
        return f"[Error Code {self.error_code}] {self.age} -> {self.msg}"

try:
    raise InvalidAgeError(150)
except InvalidAgeError as e:
    print(e)

# Output: [Error Code 1001] 150 -> Age must be between 0 and 120
```

---

## Using Standard Exceptions as Base Class

Instead of inheriting from `Exception`, you can inherit from specific built-in exceptions like `RuntimeError`, `ValueError`, etc.

```python
# Inherit from RuntimeError
class NetworkError(RuntimeError):
    def __init__(self, arg):
        self.args = (arg,)

try:
    raise NetworkError("Connection failed")
except NetworkError as e:
    print(e.args)

# Output: ('Connection failed',)
```

---

## Real-World Example: Invalid Email Error

```python
class InvalidEmailError(Exception):
    def __init__(self, email, msg="Invalid email format"):
        self.email = email
        self.msg = msg
        super().__init__(self.msg)
    
    def __str__(self):
        return f"{self.email} -> {self.msg}"

def set_email(email):
    if "@" not in email:
        raise InvalidEmailError(email)
    print(f"Email set to: {email}")

try:
    set_email("userexample.com")
except InvalidEmailError as e:
    print(e)

# Output: userexample.com -> Invalid email format
```

---

## When to Use User-Defined Exceptions

| Scenario | Example |
|----------|---------|
| **Application-specific errors** | `InsufficientFundsError`, `InvalidAgeError` |
| **Clearer error messages** | `"Balance cannot be negative"` instead of generic `ValueError` |
| **Group related errors** | Catching `DatabaseError` that covers connection, query, timeout errors |
| **Add extra context** | Include error codes, invalid values, timestamps |
| **Better debugging** | Custom error messages with specific details |

---

## Key Points

### ✅ **Benefits**
- **Readability**: Clear, self-documenting error types
- **Maintainability**: Centralized error handling
- **Specificity**: Catch exactly what you need
- **Context**: Add useful information (error codes, values)

### ⚠️ **Best Practices**
1. **Always inherit from `Exception`** (not `BaseException`)
2. **Use descriptive names** ending with "Error" (e.g., `ValidationError`)
3. **Provide meaningful error messages**
4. **Add useful attributes** (error codes, invalid values)
5. **Override `__str__`** for readable output
6. **Document when exceptions are raised** in function docstrings

---

## Quick Template

```python
class CustomError(Exception):
    """Custom exception for application-specific errors"""
    
    def __init__(self, value, message="Custom error occurred", error_code=1000):
        self.value = value
        self.message = message
        self.error_code = error_code
        super().__init__(self.message)
    
    def __str__(self):
        return f"[Error {self.error_code}] {self.value} -> {self.message}"

# Usage
try:
    raise CustomError(42, "Invalid value provided", 1001)
except CustomError as e:
    print(e)  # Output: [Error 1001] 42 -> Invalid value provided
```

---

User-defined exceptions make your code more robust, readable, and maintainable by providing meaningful error handling specific to your application's needs!
