# Class Methods in Python

In Object-Oriented Programming (OOP), a **class method** is a method that **operates on the class itself**, rather than on individual objects.
It is defined using the `@classmethod` decorator.

---

## 🧩 1. What is a Class Method?

* Class methods **access or modify class-level attributes** (shared by all instances).
* They take `cls` as the first parameter, which refers to the **class**, not an object.
* Can be called **using the class name or an object**.

**Syntax:**

```python
@classmethod
def method_name(cls, parameters):
    # method body
```

---

## 🧠 2. Example of a Class Method

```python
class Person:
    species = "Homo sapiens"  # class attribute

    def __init__(self, name):
        self.name = name  # instance attribute

    @classmethod
    def show_species(cls):
        print(f"All humans belong to the species: {cls.species}")

# Calling class method using the class
Person.show_species()  
# Output: All humans belong to the species: Homo sapiens

# Calling class method using an object
person1 = Person("Alice")
person1.show_species()  
# Output: All humans belong to the species: Homo sapiens
```

---

## 🔍 3. Key Points

| Concept          | Description                                                                |
| ---------------- | -------------------------------------------------------------------------- |
| **Class Method** | A method that operates on the class rather than an instance                |
| **cls**          | Refers to the class itself, used instead of `self`                         |
| **Decorator**    | `@classmethod` marks a method as a class method                            |
| **Usage**        | Access or modify **class attributes**, can be called using class or object |

---

✅ **In short:**

> Class methods allow you to interact with **class-level data**, not instance-level data, and are marked with `@classmethod`.

---
