---
layout: quote
---

# Shorthand Assignment Operators

When modifying a variable based on its current value:

````md magic-move {lines:true}
```python {*|2}
score = 5
score = score + 1   # Long way
```

```python {2}
score = 5
score = 5 + 1   # Long way
```

```python {2}
score = 5
score = 6   # Long way
```

```python {2}
score = 5
score = score + 1   # Long way
```

```python {2}
score = 5
score += 1          # Shorthand (same result)
```

```python {*}
score = 5
score = score + 1   # Long way
score += 1          # Shorthand (same result)
```
````


---
layout: quote
---

# All Shorthand Operators

There is a shorthand for every math operator:

```python {*|1|2|3|4}
x += 5    # x = x + 5
x -= 5    # x = x - 5
x *= 5    # x = x * 5
x /= 5    # x = x / 5
```


---
layout: quote
---

# Shorthand: += and -=

````md magic-move {lines:true}
```python {*|2}
x = 10
x += 5
x -= 3
```

```python {2}
x = 10
x = x + 5
x -= 3
```

```python {2}
x = 10
x = 10 + 5
x -= 3
```

```python {2|3}
x = 10
x = 15
x -= 3
```

```python {3}
x = 10
x = 15
x = x - 3
```

```python {3}
x = 10
x = 15
x = 15 - 3
```

```python {3}
x = 10
x = 15
x = 12
```

```python {*}
x = 10
x += 5
x -= 3
```
````


---
layout: quote
---

# Shorthand: *= and /=

````md magic-move {lines:true}
```python {*|2}
x = 10
x *= 5
x /= 4
```

```python {2}
x = 10
x = x * 5
x /= 4
```

```python {2}
x = 10
x = 10 * 5
x /= 4
```

```python {2|3}
x = 10
x = 50
x /= 4
```

```python {3}
x = 10
x = 50
x = x / 4
```

```python {3}
x = 10
x = 50
x = 50 / 4
```

```python {3}
x = 10
x = 50
x = 12.5
```

```python {*}
x = 10
x *= 5
x /= 4
```
````
