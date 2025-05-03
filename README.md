# Introduction to Variables, Constants, Scope, and Data Types in Python

## ⏰ 15-Minute Lesson Plan

**Audience:** BTEC IT Students
**Goal:** Understand constants vs variables, local vs global variables, and basic data types in Python.

---

## 🗣️ Part 1 – Introduction (1 min)

> *"Hi everyone! Today, we’re going to learn about something fundamental in programming — **variables, constants, and data types**. These are the building blocks for writing any program. Let's dive in!"*

---

## 🔹 Part 2 – Constants & Variables (3 mins)

### ✅ What is a Variable?

A **variable** is a named storage for data. You can **change its value** later in the code.

```python
name = "Tom"
age = 17
```

> 🧠 Think of variables like **labeled boxes**. You can put something inside, and even swap it out later.

### 🔒 What is a Constant?

A **constant** is a value that should **not change** once assigned. Python doesn’t enforce constants, but we **use ALL CAPS** to name them.

```python
PI = 3.14159
```

> 📌 *"In real life, PI doesn’t change. That’s why we treat it as a constant."*

---

## 🔹 Part 3 – Local vs Global Variables (4 mins)

### 🌍 Global Variables

* Defined **outside** of any function.
* Can be accessed anywhere in the file.

```python
global_message = "Hello"

def greet():
    print(global_message)  # Accessible here
```

### 🧪 Local Variables

* Defined **inside** a function.
* Only work **inside** that function.

```python
def say_hello():
    name = "Alice"  # Local variable
    print(name)

print(name)  # ❌ Error: name is not defined
```

### ⚠️ To Modify a Global Variable

Use the `global` keyword:

```python
count = 0

def increase():
    global count
    count += 1
```

> 🧠 *"If you don’t use `global`, Python thinks you're creating a **new local variable**."*

---

## 🔹 Part 4 – Data Types (5 mins)

Python has several built-in data types. Here are five key ones:

| Type      | Example         | Description                            |
| --------- | --------------- | -------------------------------------- |
| Integer   | `10`, `-3`      | Whole numbers                          |
| Real      | `3.14`, `-2.5`  | Also called floats; decimal values     |
| String    | `"Hello"`       | Sequence of characters                 |
| Character | `'A'`           | A single letter (just a 1-char string) |
| Boolean   | `True`, `False` | True/False values                      |

```python
name = "Jake"        # string
grade = 85           # integer
percentage = 85.5    # real (float)
passed = True        # boolean
initial = 'J'        # character
```

> 💡 In Python, we don’t need to declare the type — it figures it out for us!

---

## 💻 Part 5 – Mini Live Coding Demo (2 mins)

```python
PI = 3.14                  # Constant
student_name = "Sam"      # String
score = 90                # Integer
passed = True             # Boolean

def print_details():
    message = "Well done!"   # Local variable
    print(student_name)      # Global variable
    print(score)
    print(message)

print_details()
```

---

## 🌟 Recap & Quiz (30 seconds)

**Quick Quiz Questions:**

1. What’s the difference between a constant and a variable?
2. What happens if you try to access a local variable outside its function?
3. Name 3 different data types.

> 📚 **Final Tip**: *"Whenever you write code, always think: **Where does this variable live?** and **What type of data is it holding?** These two questions will guide your debugging and help you write cleaner code."*
