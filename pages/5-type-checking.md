---
layout: quote
---

# Type Errors and Type Checking

The Type Error Problem

```python
num_chars = len(input("What is your name? "))
print("Your name has " + num_chars + " characters")
```

**ERROR!** You can't concatenate a string with an integer.

---
layout: quote
---


# Checking Data Types

Use `type()` to check what type something is:

```python
print(type("Hello"))    # <class 'str'>
print(type(123))        # <class 'int'>
print(type(3.14))       # <class 'float'>
```

[TRY IT] What type is `type(len("Hello"))`? And what about `type(3.14)`?