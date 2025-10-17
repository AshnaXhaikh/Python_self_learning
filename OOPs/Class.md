# Class in Python

A **class** is one of the core concepts of Object-Oriented Programming (OOP).
It acts as a **blueprint** or **template** for creating objects.
A class defines the **structure (attributes)** and **behavior (methods)** that its objects will have.

---

## 🧩 1. What is a Class?

* A **class** groups related data and functions together.
* It helps you model real-world entities — like a *Car*, *Person*, or *Student*.
* You can create many **objects** from a single class.

**Syntax:**

```python
class ClassName:
    # class body
    # attributes and methods go here
    pass
```

---

## 🧠 2. Example

```python
class Person:
    def __init__(self, name, age):
        self.name = name    # attribute
        self.age = age      # attribute

    def greet(self):        # method
        print(f"Hello, my name is {self.name} and I am {self.age} years old.")
```

Here:

* `Person` → is a **class**.
* `name` and `age` → are **attributes**.
* `greet()` → is a **method**.
* The `__init__()` function → initializes new objects.
* The `self` keyword → refers to the current object.

---

## 🚀 3. Creating an Object from a Class

```python
person1 = Person("Alice", 25)
person1.greet()
```

**Output:**

```
Hello, my name is Alice and I am 25 years old.
```

---

## 🔍 4. Key Points

| Concept        | Description                                         |
| -------------- | --------------------------------------------------- |
| **Class**      | Blueprint or template for creating objects          |
| ****init****   | Special method used to initialize object attributes |
| **self**       | Refers to the current instance of the class         |
| **Attributes** | Variables inside a class that store data            |
| **Methods**    | Functions inside a class that define behavior       |

---

## 🧾 5. Why Use Classes?

* Organize and reuse code easily
* Model real-world entities
* Keep data and behavior together
* Support OOP principles like **encapsulation** and **inheritance**

---

✅ **In short:**

> A **class** defines what an object will be — its properties and actions — while the **object** is the actual thing created from that class.

---

