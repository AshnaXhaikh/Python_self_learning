# Static Methods in Python

In Object-Oriented Programming (OOP), a **static method** is a method that **does not operate on the instance or class**.
It is independent of object or class attributes and is defined using the `@staticmethod` decorator.

---

## 🧩 1. What is a Static Method?

* Static methods **do not take `self` or `cls`** as the first parameter.
* They behave like **regular functions**, but belong to a class’s namespace.
* Useful for **utility functions** related to a class but not needing instance or class data.

**Syntax:**

```python
@staticmethod
def method_name(parameters):
    # method body
```

---

## 🧠 2. Example of a Static Method

```python
class MathOperations:
    
    @staticmethod
    def add(a, b):
        return a + b
    
    @staticmethod
    def multiply(a, b):
        return a * b

# Calling static methods using the class
print(MathOperations.add(5, 3))       # Output: 8
print(MathOperations.multiply(5, 3))  # Output: 15

# Calling static methods using an object
math_obj = MathOperations()
print(math_obj.add(10, 7))            # Output: 17
```

---

## 🔍 3. Key Points

| Concept           | Description                                                             |
| ----------------- | ----------------------------------------------------------------------- |
| **Static Method** | A method that does not depend on the instance (`self`) or class (`cls`) |
| **Decorator**     | `@staticmethod` marks a method as static                                |
| **Usage**         | Useful for utility or helper functions related to a class               |
| **Access**        | Can be called using the class or an object                              |

---

✅ **In short:**

> Static methods are **class-related utility functions** that don’t need access to instance or class data.

---
