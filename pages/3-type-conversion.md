---
layout: quote
---


# Type Conversion

You can convert between types using these functions:

| Function | Converts to |
| --- | --- |
| `str()` | String |
| `int()` | Integer |
| `float()` | Float |

---
layout: quote
---


# Type Conversion Examples


**String to Integer**
```python
age_str = "25"
age_int = int(age_str)
print(age_int + 5)   # 30
```

**Integer to String**
```python
num = 100
text = str(num)
print("Score: " + text)   # Score: 100
```

**String to Float**
```python
# String to Float
price = float("19.99")
print(price * 2)   # 39.98
```

---
layout: quote
---


# But why bother with the conversion?

In real life you won’t be given the type of your choice so you need to be able to change the data in your desired type

---
layout: quote
---

# Type Conversion: Practical Example

```python
# I want to add 10 to '$150'

price = '$150'
print(f'Original price: {price}')

# first remove $ so the values becomes '150'
remove_dollar = price.replace('$', '') 

# then convert it to an int so it becomes 150
num_price = int(remove_dollar)

# add 10 to the 'clean' price
new_price = num_price + 10

# convert back to string and add the removed dollar sign
# so we started from '$150' and ended with '$160'
price = '$' + str(new_price)
print(f'New price: {price}')

```

---
layout: quote
---

# The input() Function Always Returns a String!

```python
age = input("How old are you? ")   # User types 25
print(type(age))                    # <class 'str'> - it's a string!

age = int(input("How old are you? "))   # Now it's an integer
print(type(age))                         # <class 'int'>
```

[QUESTION] Why does `input()` return a string? Because users can type anything!