---
layout: quote
---

# Formatting Numbers

For money, you want exactly 2 decimal places:

```python
total = 15.5
print(f"Total: ${total}")       # $15.5
print(f"Total: ${total:.2f}")   # $15.50

```

The `:.2f` means "format as float with 2 decimal places."


---
layout: quote
---

# Formatting Numbers Example

```python
price = 19.99
tax = price * 0.08
total = price + tax
print(f"Price: ${price:.2f}")
print(f"Tax: ${tax:.2f}")
print(f"Total: ${total:.2f}")

```

[TRY IT] Run this. Try changing the price.