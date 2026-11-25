---
layout: quote
---

# Quotes and Escape Characters

### Single Quotes vs Double Quotes

Both `'` and `"` create strings — they're interchangeable:

```python
print("Hello, World!")   # double quotes
print('Hello, World!')   # single quotes — same output
```


---
layout: quote
---

# Quotes

The reason Python has both is so you can put quote characters *inside* your string. The rule is simple:

- Wrap in `"..."` when your string contains `'`
- Wrap in `'...'` when your string contains `"`

```python
print("It's a beautiful day.")               # ✅ single quote inside double
print('He said, "Python is great!"')         # ✅ double quote inside single
print('It's a beautiful day.')               # ❌ ERROR — Python gets confused
```

---
layout: quote
---

# Escaping with Backslash

What if you need *both* kinds of quotes? Prefix the quote with `\` to escape it:

```python
print('It\'s a beautiful \"day\".')   # ✅ escaped quotes
```

The backslash tells Python: *treat the next character as literal text, not as string syntax*.

---
layout: quote
---

# The `\n` Newline

`\n` is an **escape sequence** — it represents a line break:

```python
print('a\nb\nc')
# a
# b
# c
```

Every `print()` automatically adds `\n` at the end. You can change this with `end=`:

```python
print("Sue", end='')   # no newline — next print continues on the same line
print("Smith")
# SueSmith
```

---
layout: quote
---

# Escape Sequences

Other useful escape sequences:

- `\n` — new line
- `\t` — tab (indentation)
- `\\` — literal backslash
- `\'` — literal single quote
- `\"` — literal double quote

[QUESTION] What does `print("Hello", end=' ')` do differently from plain `print("Hello")`?

---
layout: quote
---

# Exercise: Fix the Quotes

Each line below has a quote error. Fix all three without changing the message.

```python
# Fix the quote error in each line

print('It's a beautiful day')         # broken
print("She said "Python is fun"")     # broken
print('He's saying "Hello" to her')   # broken
```

---
layout: quote
---

# Solution
    
```python
print("It's a beautiful day")
print('She said "Python is fun"')
print("He's saying \"Hello\" to her")   # or: print('He\'s saying "Hello" to her')
```
    

[QUESTION] The last line has two valid solutions. What's the difference between them?

---
layout: quote
---

# Exercise: One Print, Four Lines

Prints four lines of information using a single `print()` statement.

Expected output:

```
Name: Alice
Age: 28
City: London
Job: Developer
```

---
layout: quote
---

# Solution

```python
print("Name: Alice\nAge: 28\nCity: London\nJob: Developer")
```
    
