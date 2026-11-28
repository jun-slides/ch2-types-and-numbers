---
layout: quote
---

# Python Data Types

Not all data is the same. Python has different **data types** for different kinds of information.


<v-clicks>

| Data Type | Description | Example |
| --- | --- | --- |
| **String** | Text (characters) | `"Hello"`, `"123"` |
| **Integer** | Whole numbers | `42`, `-17`, `0` |
| **Float** | Decimal numbers | `3.14`, `-0.5` |

</v-clicks>

---
layout: quote
---

# Strings (str)

A string is a "string of characters" - text wrapped in quotes:

<v-clicks>

```python
"Hello"        # String
'Hello'        # Also a string
"123"          # This is a STRING, not a number!
```

**Important:** `"123"` is text, not a number. You can't do math with it!

```python
print("10" + "20")   # Outputs: 1020(concatenation)
print(10 + 20)       # Outputs: 30 (addition)
```

</v-clicks>

---
layout: quote
---

# Integers (int)

Whole numbers without decimal points:


<v-clicks>


```python
age = 28
year = 2026
negative = -50
```

**Tip:** For large numbers, use underscores for readability:

```python
population = 7_900_000_000    # Same as 7900000000
```

</v-clicks>


---
layout: quote
---

# Floats (float)

Numbers with decimal points (floating-point numbers):

```python
pi = 3.14159
height = 1.75
price = 19.99
```