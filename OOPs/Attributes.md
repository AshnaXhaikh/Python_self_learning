# Attributes in Python

In Object-Oriented Programming (OOP), **attributes** are **variables associated with an object**.
They represent the **properties or data** that belong to a class or its objects.

---

## 🧩 1. What are Attributes?

* Attributes store information about an object.
* They define the **state or properties** of the object.
* In Python, attributes are usually defined inside the `__init__` method using the **`self`** keyword.

**Syntax:**

```python
self.attribute_name = value
```

---

## 🧠 2. Example of Attributes

```python
class Person:
    def __init__(self, name, age):
        self.name = name  # attribute
        self.age = age    # attribute

# Creating objects
person1 = Person("Alice", 25)
person2 = Person("Bob", 30)

# Accessing attributes
print(person1.name)  # Output: Alice
print(person2.age)   # Output: 30
```

Here:

* `name` and `age` are **attributes** of the `Person` class.
* Each object has its **own copy** of these attributes.

---

## 🧩 3. Types of Attributes

1. **Instance Attributes**

   * Defined inside `__init__` using `self`.
   * Belong to individual objects.

   ```python
   self.name = name
   ```

2. **Class Attributes**

   * Defined directly inside the class (outside `__init__`).
   * Shared across all objects of the class.

   ```python
   class Person:
       species = "Homo sapiens"  # class attribute
   ```

**Example:**

```python
print(Person.species)      # Homo sapiens
print(person1.species)     # Homo sapiens
```

---

## 🔍 4. Key Points

| Concept                | Description                        |
| ---------------------- | ---------------------------------- |
| **Attribute**          | A variable belonging to an object  |
| **Instance Attribute** | Belongs to a specific object       |
| **Class Attribute**    | Shared by all objects of the class |
| **self**               | Refers to the current object       |

---

✅ **In short:**

> Attributes are used to store data about objects, defining their properties and state.

---
