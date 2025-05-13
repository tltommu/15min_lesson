# This is not the most updated version of the md file, please refer to the kaggle notebook for the most updated version.

# 🎓 Introduction to Variables, Constants, Scope, and Data Types in Python

---

## 🗣️ Part 1 – Introduction (1 min)

"Hi everyone! Today, we’re going to learn about something fundamental in programming — variables, constants, and data types. These are the building blocks for writing any program. Let's dive in!"

---

## 🔹 Part 2 – Data Types (5 mins)

Python has several built-in data types. Here are five key ones:

| Type      | Example   | Description                  |
|-----------|-----------|------------------------------|
| Integer   | 10, -3     | Whole numbers                |
| Float     | 3.14, -2.5 | Decimal values               |
| String    | "Hello"    | Sequence of characters       |
| Character | 'A'        | A single letter              |
| Boolean   | True, False| True/False values            |

### python variable declaration and their types

```
name3 = "Jake"        # string
grade = 85           # integer
percentage = 85.5    # double (float)
passed = True        # boolean
initial = 'J'        # character

print(name3)
print(grade)
print(percentage)
print(passed)
print(initial)

print(type(name3))
print(type(grade))
print(type(percentage))
print(type(passed))
print(type(initial))
````

### output via kaggle

```
Jake
85
85.5
True
J
<class 'str'>
<class 'int'>
<class 'float'>
<class 'bool'>
<class 'str'>
```

💡 In Python, we don’t need to declare the type — it figures it out for us!
🧠 (Why do people say Python code is slow? It's partly because of dynamic typing.)

---

## 🔹 Part 3 – Constants & Variables (3 mins)

### ✅ What is a Variable?

A variable is a named storage for data. You can change its value later in the code.

```python
name = "Tom"  # automatically a string
age = 17      # automatically an integer

print(name)
print(age)
```

**Output:**

```
Tom
17
```

🧠 Think of variables like labeled boxes. You can put something inside, and even swap it out later.

---

### 🔒 What is a Constant?

A constant is a value that should not change once assigned.
Python doesn’t enforce constants, but we use **ALL CAPS** to name them.

```python
PI = 3.14159
print(PI)
```

**Output:**

```
3.14159
```

📌 "In real life, PI doesn’t change. That’s why we treat it as a constant."

---

## 🔹 Part 4 – Local vs Global Variables (4 mins)

### 🌍 Global Variables

Defined outside of any function. Can be accessed anywhere in the file.

```python
global_message = "Hello"

def greet():
    print(global_message)  # Accessible here
```

---

### 🧪 Local Variables

Defined inside a function. Only work inside that function.

```python
def say_hello():
    name2 = "Alice"  # Local variable
    print(name2)

say_hello()
print(name2)  # ❌ Error: name is not defined
```

**Output:**

```
Alice
NameError: name 'name2' is not defined
```

---

### ⚠️ To Modify a Global Variable

Use the `global` keyword:

```python
count = 0

def increase():
    global count
    count += 1

print(count)
increase()
print(count)
```

🧠 "If you don’t use `global`, Python thinks you're creating a new local variable."

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

## 💥 Part 6 – Extra Exercise (Take-home / Optional)

### 🧪 Exercise: Print Numbers 1 to 5

Write a Python for loop that prints numbers from 1 to 5 using a variable.

📌 You can Google or use ChatGPT to help you solve this.

```python
# Enter your code below
```

---

## 🌟 Recap & Quiz (30 seconds)

### Quick Quiz Questions:

1. What’s the difference between a constant and a variable?
2. What happens if you try to access a local variable outside its function?
3. Name 3 different data types.

---

📚 **Final Tip**:
"Whenever you write code, always ask yourself:

* Where does this variable live?
* What type of data is it holding?"

These two questions will guide your debugging and help you write cleaner code.

# Addtional Material: C# Examples

## 💻 Part 2 Reference:  C# Data Types where you can go to [onecompiler](https://onecompiler.com/) to try it

| Data Type | Example                         | Size  (memory)        | Description                                                |
| --------- | ------------------------------- | --------------------- | ---------------------------------------------------------- |
| int       | `int age = 18;`                 | 4 bytes               | Stores whole numbers from -2,147,483,648 to 2,147,483,647  |
| long      | `long population = 8000000000;` | 8 bytes               | Stores whole numbers from -9 quintillion to +9 quintillion |
| float     | `float pi = 3.14f;`             | 4 bytes               | Decimal (6–7 digits precision)                             |
| double    | `double price = 19.99;`         | 8 bytes               | Decimal (15 digits precision)                              |
| bool      | `bool passed = true;`           | 1 byte                | True or False                                              |
| char      | `char initial = 'T';`           | 2 bytes               | A single character                                         |
| string    | `string name = "Tom";`          | 2 bytes per character | A sequence of characters                                   |


```csharp
C#

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text.RegularExpressions;
namespace HelloWorld
{
	public class Program
	{
		public static void Main(string[] args)
		{
			string name = "Jake";
			int grade = 85;
			float percentage = 85.5f;
			bool passed = true;
			char initial = 'J';
  
          		Console.WriteLine(name); // Console.WriteLine() is the print() function for C#
          		Console.WriteLine(grade);
          		Console.WriteLine(percentage);
          		Console.WriteLine(passed);
          		Console.WriteLine(initial);
		}
	}
}
```

### output
![image](https://github.com/user-attachments/assets/95ea4a89-0c95-4653-893e-0f6e9afd87f2)

## 📚 Part 3 Reference: C# Variables & Constant

```csharp
using System;

namespace MyApplication
{
  class Program
  {
    static void Main(string[] args)
    {
      int age = 17;
      string name = "Tom";
      Console.WriteLine(age);
      Console.WriteLine(name);
    }
  }
}
```

### C# output
![image](https://github.com/user-attachments/assets/45bdee50-3df9-4a76-91f9-a6fb0590dff2)

### C# another variable example 

```
using System;

namespace MyApplication
{
  class Program
  { 
    static void Main(string[] args)
    {
      string name = "Tom3"; //declaring name as variable
      Console.WriteLine(name);
      name = "Tom2";
      Console.WriteLine(name);
    }
  }
}

```

### output (hence the output can change)
![image](https://github.com/user-attachments/assets/8a4e636a-3815-4518-84fc-6fe85b608f4a)

### C# const example
```
using System;

namespace MyApplication
{
  class Program
  { 
    static void Main(string[] args)
    {
      Const string Constname = "Tom3"; //declaring Constname as const
      Console.WriteLine(Constname);
      Constname = "Tom2";
      Console.WriteLine(Constname);
    }
  }
}
```
### output (throwing an error as we declared it Constname as Constant)
![image](https://github.com/user-attachments/assets/18e390ce-c25b-42bd-be6d-2029ecc04f8f)

## 📖 Part 4 Reference: C# Global and local example
```
using System;

namespace MyApplication
{
  class Program
  {
    // 🌍 Global variable (class-level/static field)
    static string globalMessage = "Hello from global scope";

    static void Main(string[] args)
    {
      // 🧪 Local variable (only available in Main)
      string localMessage = "Hello from local scope";

      Console.WriteLine(globalMessage);  // ✅ Works
      Console.WriteLine(localMessage);   // ✅ Works

      PrintMessages();
        //uncomment the line below and run it yourself to see if you can get my output
      // Console.WriteLine(otherLocal);  // ❌ Error: does not exist in this context
    }

    static void PrintMessages()
    {
      Console.WriteLine(globalMessage);  // ✅ Can access global
      string otherLocal = "Local inside PrintMessages";
      Console.WriteLine(otherLocal);     // ✅ Works only here
    }
  }
}
```
### output without the error line
![image](https://github.com/user-attachments/assets/79d3824f-0075-414f-90e7-68e1172e2131)



### output with the error line
![image](https://github.com/user-attachments/assets/d5b2374d-259d-485f-9ae0-119ba7e6ccd4)
