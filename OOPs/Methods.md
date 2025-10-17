# Methods in Python

In Object-Oriented Programming (OOP), **methods** are **functions defined inside a class**.
They describe the **behavior or actions** that objects of the class can perform.

---

## 🧩 1. What are Methods?

* Methods are **functions that belong to a class**.
* They can **access or modify object attributes** using the `self` keyword.
* Methods define what an object **can do**.

**Syntax:**

```python
def method_name(self, parameters):
    # method body
```

---

## 🧠 2. Example of a Method

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):  # method
        print(f"Hello, my name is {self.name} and I am {self.age} years old.")

# Creating an object
person1 = Person("Alice", 25)

# Calling a method
person1.greet()  # Output: Hello, my name is Alice and I am 25 years old.
```

Here:

* `greet()` is a **method** of the `Person` class.
* `self.name` and `self.age` are accessed inside the method to use the object’s attributes.

---

## 🧩 3. Types of Methods

1. **Instance Methods**

   * The most common type of method.
   * Access and modify **instance attributes**.

   ```python
   def greet(self):
       print(f"Hello, {self.name}")
   ```

2. **Class Methods**

   * Defined using `@classmethod`.
   * Access **class attributes** using `cls`.

   ```python
   @classmethod
   def species(cls):
       print(cls.species_name)
   ```

3. **Static Methods**

   * Defined using `@staticmethod`.
   * Do **not access instance or class attributes**.

   ```python
   @staticmethod
   def info():
       print("This is a static method")
   ```

---

## 🔍 4. Key Points

| Concept             | Description                                     |
| ------------------- | ----------------------------------------------- |
| **Method**          | Function defined inside a class                 |
| **Instance Method** | Operates on object attributes using `self`      |
| **Class Method**    | Operates on class attributes using `cls`        |
| **Static Method**   | Independent method, doesn’t use `self` or `cls` |

---

✅ **In short:**

> Methods define **what an object can do** and allow interaction with its data (attributes).

---
