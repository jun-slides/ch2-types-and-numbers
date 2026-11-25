---
layout: quote
---

# Numbers in Python

Python handles two types of numbers:

```python
age = 28          # int (whole number)
price = 19.99     # float (decimal number)

```

<v-clicks>

Basic math works as expected:

```python
10 + 3   # 13
10 - 3   # 7
10 * 3   # 30
10 / 3   # 3.333...

```

[TRY IT] Try each of these. What do you notice about division?

</v-clicks>

---
layout: quote
---



# Basic math operations

| Operator | Operation | Example |
| --- | --- | --- |
| `+` | Addition | 5 + 3 = 8 |
| `-` | Subtraction | 5 - 3 = 2 |
| `*` | Multiplication | 5 * 3 = 15 |
| `/` | Division | 5 / 3 = 1.666... |

---
layout: quote
---


# Exercise

````md magic-move {lines:true}
```python
# Problem 1: Write the code to add 10 and 15.


# Problem 2: Write the code to subtract 8 from 15.


# Problem 3: Write the code to multiply 7 by 6.


# Problem 4: Write the code to divide 8 by 3.

```

```python
# Problem 1: Write the code to add 10 and 15.
print(10 + 15)

# Problem 2: Write the code to subtract 8 from 15.


# Problem 3: Write the code to multiply 7 by 6.


# Problem 4: Write the code to divide 8 by 3.

```

```python
# Problem 1: Write the code to add 10 and 15.
print(10 + 15)

# Problem 2: Write the code to subtract 8 from 15.
print(15 - 8)

# Problem 3: Write the code to multiply 7 by 6.


# Problem 4: Write the code to divide 8 by 3.

```

```python
# Problem 1: Write the code to add 10 and 15.
print(10 + 15)

# Problem 2: Write the code to subtract 8 from 15.
print(15 - 8)

# Problem 3: Write the code to multiply 7 by 6.
print(7 * 6)

# Problem 4: Write the code to divide 8 by 3.

```

```python
# Problem 1: Write the code to add 10 and 15.
print(10 + 15)

# Problem 2: Write the code to subtract 8 from 15.
print(15 - 8)

# Problem 3: Write the code to multiply 7 by 6.
print(7 * 6)

# Problem 4: Write the code to divide 8 by 3.
print(8 / 3)
```

````
    


    

---
layout: quote
---

# More Math Operators

Operations you might not be familiar with

<v-clicks>

| Operator | Operation | Example |
| --- | --- | --- |
| `**` | Exponent (power) | 5 ** 3 = 125 |
| `%` | Modulo (remainder) | 5 % 3 = 2 |
| `//` | Floor division | 5 // 3 = 1 |

</v-clicks>

---
layout: quote
---


# Division Always Returns a Float

```python
print(10 / 2)    # 5.0 (not 5)
print(10 // 2)   # 5 (floor division gives integer)
```

---
layout: quote
---



# Order of Operations:  PEMDAS / GEMS

Python evaluates expressions based on operator priority — 
<br>
Higher-priority operators run first. 
<br>
Operators at the same priority level are evaluated left to right.

1. **`()` P**arentheses / **G**rouping
2. `**` **E**xponents
3. **`*`, `/` M**ultiplication / **D**ivision  and also `//`, `%`
4. **`-`, `+` S**ubtraction / **A**ddition 

Example

````md magic-move {lines:true}
```python {*|1}
print(3 * 3 + 3 / 3 - 3)   
print(3 * (3 + 3) / 3 - 3) 
```

```python {1}
print(9 + 3 / 3 - 3)   
print(3 * (3 + 3) / 3 - 3) 
```

```python {1}
print(9 + 1.0 - 3)   
print(3 * (3 + 3) / 3 - 3) 
```

```python {1|2}
print(7.0)   
print(3 * (3 + 3) / 3 - 3) 
```

```python {2}
print(7.0)   
print(3 * 6 / 3 - 3) 
```

```python {2}
print(7.0)   
print(18 / 3 - 3) 
```

```python {2}
print(7.0)   
print(6.0 - 3) 
```

```python {2|*}
print(7.0)   
print(3.0) 
```

```python 
print(3 * 3 + 3 / 3 - 3)    # Output:  7.0
print(3 * (3 + 3) / 3 - 3)  # Output:  3.0
```
````

<v-click>

[TRY IT] What's the result of `2 ** 3 * 2`?
</v-click>
