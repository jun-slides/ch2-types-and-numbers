---
layout: quote
---


## Part 4: Getting Numbers from Input

`input()` always returns text. To do math, convert it:

```python
age = input("How old are you? ")
print(age + 10)  # This will ERROR!

```

[PREDICT] Why does this fail?


---
layout: quote
---


# **Fix it with `int()` or `float()`:**

```python
age = int(input("How old are you? "))
print(age + 10)  # Now it works!

```

```python
price = float(input("Enter price: "))
print(price * 2)

```

[QUESTION] When would you use `int()` vs `float()`?