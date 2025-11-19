# Technical Paper on Python, SQL & HTML Concepts

---

1. How Python Manages Memory

- Python uses a private heap memory area to store objects. The memory management is automatically handled by:

- Key Mechanisms

    - Reference Counting: Each object keeps track of how many references point to it. When count becomes zero, memory is freed.

    - Garbage Collector: Handles cyclic references (objects referencing each other).

    - Memory Manager: Allocates and deallocates memory blocks internally.

    - Object-Specific Allocators: For integers, strings, lists etc. to optimize speed.

- Simple Example

``` python
    a = 10
    b = a   ' reference count increases '
    del a   ' reference count decreases '
```

- Real-Life Example

    - It’s like a library:
        - Books (objects) stay on shelves as long as someone has borrowed them (references). When no one needs a book anymore, it is removed from the active shelf (garbage collected).

---

2. Why We Use *args and **kwargs in Python

- Definitions

- *args allows passing any number of positional arguments.

- **kwargs allows passing any number of keyword arguments.

- Simple Example

``` python
    def example(*args, **kwargs):
        print(args)
        print(kwargs)

    example(1, 2, name="Pratik", age=21)
```

- Real-Life Example

    - Think of *args as a flexible seat in a car that can hold 1, 2, or more passengers.
    - **kwargs is like writing each passenger’s label: "Driver=John", "Navigator=Sam".

---

3. Block vs Inline Elements in HTML

- Block Elements:

    - Start on a new line

    - Occupy full width by default

    - Examples: ` <div>, <p>, <h1>, <section> `

- Inline Elements:

    - Do not start on a new line

    - Occupy only the width they need

    - Examples: ` <span>, <a>, <strong> `

- Simple Example:

``` python
<p>This is block</p>
<span>This is inline</span>
```

- Real-Life Example:

    - Block elements are like full-width containers (rooms).
    - Inline elements are like small items inside a room (books, cups).

---

4. What Are Decorators in Python?

- A decorator modifies the behavior of a function without changing its code.

- Simple Example:

```python
    def logger(func):
        def wrapper():
            print("Function called")
            return func()
        return wrapper

    @logger
    def greet():
        print("Hello")

    greet()
```

- Real-Life Example:

    - Decorators are like adding a wrapper around a gift—it adds extra functionality without changing the gift itself.

---

5. Does Python Support Method Overloading?

- No, Python does not support traditional method overloading.

- If multiple methods with the same name are defined, the latest one overrides the previous.

- Workaround Using Default Arguments:

``` python
    def add(a, b=0, c=0):
        return a + b + c
```

- Real-Life Example:

    - Like a restaurant menu where you cannot have two dishes with the same name unless you use optional ingredients.

---

6. Pattern Matching in SQL

- Pattern matching is done using the LIKE operator and wildcards.

- Wildcards:

    - % : matches any number of characters

    - _ : matches one character

- Example:

``` sql
    SELECT * FROM employees
    WHERE name LIKE 'AM%';   ' Names starting with A '
```

---

7. SQL Operators

- Types of SQL Operators:

    - Arithmetic: +, -, *, /

    - Comparison: =, <, >, <=, >=, <>

    - Logical: AND, OR, NOT

    - Bitwise (depends on DB)

    - Special: IN, BETWEEN, LIKE, IS NULL

---

8. Aggregate Functions in SQL

- Aggregate functions compute summary values.

- Common Ones:

    - COUNT()

    - SUM()

    - AVG()

    - MIN(), MAX()

- Simple Example:

``` sql
SELECT COUNT(*) FROM orders;
```

- Real-Life Example:

    - Amazon counts how many orders were placed today.

---

9. What Is the __init__ Function in Python?

- `__init__` is the constructor method of a class.
- It initializes object attributes when an object is created.

- Example

``` python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

- Real-Life Example

    - When you get a new phone, the initial setup is the __init__ process.

---

10. How to Add a Link in HTML

``` html
<a href="https://example.com">Click Here</a>
```

- Attributes

    - href : URL

    - target="_blank" : open in new tab

---

11. What Is a Constraint in SQL?

- A constraint enforces rules on a database table to ensure data integrity.

- Common Constraints:

    - PRIMARY KEY

    - FOREIGN KEY

    - UNIQUE

    - NOT NULL

    - CHECK

    - DEFAULT

- Simple Example

``` sql
age INT CHECK(age >= 18)
```

- Real-Life Example:

    - A bank preventing an account from having a negative balance is a constraint.

---
