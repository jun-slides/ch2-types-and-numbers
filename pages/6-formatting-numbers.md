---
layout: quote
---

# Formatting Numbers

For money, you want exactly 2 decimal places:

````md magic-move {lines:true}
```python {*|2}
total = 15.5
print(f"Total: ${total}")       # $15.5
print(f"Total: ${total:.2f}")   # $15.50
```

```python {2}
total = 15.5
print(f"Total: ${15.5}")       # $15.5
print(f"Total: ${total:.2f}")   # $15.50
```

```python {2|3}
total = 15.5
print(f"Total: $15.5")       # $15.5
print(f"Total: ${total:.2f}")   # $15.50
```

```python {3}
total = 15.5
print(f"Total: $15.5")       # $15.5
print(f"Total: ${15.5:.2f}")   # $15.50
```

```python {3}
total = 15.5
print(f"Total: $15.5")       # $15.5
print(f"Total: $15.50")   # $15.50
```

```python {*}
total = 15.5
print(f"Total: ${total}")       # $15.5
print(f"Total: ${total:.2f}")   # $15.50
```
````

The `:.2f` means "format as float with 2 decimal places."


---
layout: quote
---

# Formatting Numbers Example

````md magic-move {lines:true}
```python {*|2}
price = 19.99
tax = price * 0.08
total = price + tax
print(f"Price: ${price:.2f}")
print(f"Tax: ${tax:.2f}")
print(f"Total: ${total:.2f}")
```

```python {2}
price = 19.99
tax = 19.99 * 0.08
total = price + tax
print(f"Price: ${price:.2f}")
print(f"Tax: ${tax:.2f}")
print(f"Total: ${total:.2f}")
```

```python {2|3}
price = 19.99
tax = 1.5992
total = price + tax
print(f"Price: ${price:.2f}")
print(f"Tax: ${tax:.2f}")
print(f"Total: ${total:.2f}")
```

```python {3}
price = 19.99
tax = 1.5992
total = 19.99 + 1.5992
print(f"Price: ${price:.2f}")
print(f"Tax: ${tax:.2f}")
print(f"Total: ${total:.2f}")
```

```python {3|4}
price = 19.99
tax = 1.5992
total = 21.589199999999998
print(f"Price: ${price:.2f}")
print(f"Tax: ${tax:.2f}")
print(f"Total: ${total:.2f}")
```

```python {4}
price = 19.99
tax = 1.5992
total = 21.589199999999998
print(f"Price: ${19.99:.2f}")
print(f"Tax: ${tax:.2f}")
print(f"Total: ${total:.2f}")
```

```python {4|5}
price = 19.99
tax = 1.5992
total = 21.589199999999998
print(f"Price: $19.99")
print(f"Tax: ${tax:.2f}")
print(f"Total: ${total:.2f}")
```

```python {5}
price = 19.99
tax = 1.5992
total = 21.589199999999998
print(f"Price: $19.99")
print(f"Tax: ${1.5992:.2f}")
print(f"Total: ${total:.2f}")
```

```python {5|6}
price = 19.99
tax = 1.5992
total = 21.589199999999998
print(f"Price: $19.99")
print(f"Tax: $1.60")
print(f"Total: ${total:.2f}")
```

```python {6}
price = 19.99
tax = 1.5992
total = 21.589199999999998
print(f"Price: $19.99")
print(f"Tax: $1.60")
print(f"Total: ${21.589199999999998:.2f}")
```

```python {6}
price = 19.99
tax = 1.5992
total = 21.589199999999998
print(f"Price: $19.99")
print(f"Tax: $1.60")
print(f"Total: $21.59")
```

```python {*}
price = 19.99
tax = price * 0.08
total = price + tax
print(f"Price: ${price:.2f}")
print(f"Tax: ${tax:.2f}")
print(f"Total: ${total:.2f}")
```
````
