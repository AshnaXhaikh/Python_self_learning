# Instance and Object in Python

In Object-Oriented Programming (OOP), **classes** are used to create **objects**.
Each object is an **instance** of a class. This README explains the difference and relationship between **instance** and **object**.

---

## 🧩 1. Object

* An **object** is a **real entity** created from a class.
* It exists in memory and has actual values for the attributes defined in the class.

**Example:**

```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

car1 = Car("Toyota", "Corolla")
car2 = Car("Honda", "Civic")
```

Here:

* `car1` and `car2` are **objects** of the class `Car`.

---

## 🧩 2. Instance

* An **instance** is the **relationship** between the object and the class it belongs to.
* Every object created from a class is an **instance** of that class.

**Example:**

```python
print(isinstance(car1, Car))  # True
print(isinstance(car2, Car))  # True
```

Here:

* `car1` and `car2` are **instances** of the class `Car`.
* This shows that these objects **belong to the Car class**.

---

## 🧠 3. Difference Between Object and Instance

| Term         | Meaning                                           | Focus                     |
| ------------ | ------------------------------------------------- | ------------------------- |
| **Object**   | The actual thing created from a class             | The real entity in memory |
| **Instance** | The relationship between the object and its class | Belongs to a class        |

✅ **In short:**

> “`car1` is an **object** of the class `Car`, and also an **instance** of that class.”

---

## 🚀 4. Complete Example

```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

car1 = Car("Toyota", "Corolla")
car2 = Car("Honda", "Civic")

# Objects
print(car1)  # <__main__.Car object at 0x...>
print(car2)  # <__main__.Car object at 0x...>

# Instances
print(isinstance(car1, Car))  # True
print(isinstance(car2, Car))  # True
```

---

✅ **Key Takeaway:**

* **Objects** = the things you create
* **Instances** = those things belonging to a specific class

---

If you want, I can also **suggest a perfect README file name** for this so it stays consistent with your OOP series. Do you want me to do that?
