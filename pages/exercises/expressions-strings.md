---
layout: quote
---

# String Expressions

<v-clicks>

You already know how to join strings with `+`, repeat them with `*`, and change them with methods like `.upper()`. Mix these and you get a **string expression**: Python works it out to a single **new string**.

</v-clicks>

<table v-click="4">
  <thead>
    <tr v-click><th>Ingredient</th><th>Example</th><th>Works out to</th></tr>
  </thead>
  <tbody>
    <tr v-click><td>String</td><td><code>"ant"</code></td><td>itself</td></tr>
    <tr v-click><td>Variable</td><td><code>pet</code></td><td>the string stored in it</td></tr>
    <tr v-click><td>Join</td><td><code>"ab" + "cd"</code></td><td><code>"abcd"</code></td></tr>
    <tr v-click><td>Repeat</td><td><code>"ab" * 3</code></td><td><code>"ababab"</code></td></tr>
    <tr v-click><td>Method call</td><td><code>"ant".upper()</code></td><td><code>"ANT"</code></td></tr>
  </tbody>
</table>


---
layout: quote
---

# Variables in String Expressions

<v-click>

Just like with numbers, Python swaps each variable for the string stored in it:

</v-click>

````md magic-move {lines:true}
```python {*|4}
first = "Ada"
last = "Lovelace"

print(first + " " + last)
```

```python {4}
first = "Ada"
last = "Lovelace"

print("Ada" + " " + "Lovelace")
```

```python {4}
first = "Ada"
last = "Lovelace"

print("Ada Lovelace")
```

```python {*}
first = "Ada"
last = "Lovelace"

print(first + " " + last)   # Ada Lovelace
```
````



---
layout: quote
---

# Methods Are Part of the Expression

<v-click>

A method call is a lot like a function call such as `len()`: it gives back a value. For string methods that value is a new string, so you can use it anywhere a string could go:

</v-click>

````md magic-move {lines:true}
```python {*|3}
name = "sam"

print(name.upper() + "!")
print("Hi " + name.title())
```

```python {3}
name = "sam"

print("sam".upper() + "!")
print("Hi " + name.title())
```

```python {3}
name = "sam"

print("SAM" + "!")
print("Hi " + name.title())
```

```python {3|4}
name = "sam"

print("SAM!")
print("Hi " + name.title())
```

```python {4}
name = "sam"

print("SAM!")
print("Hi " + "sam".title())
```

```python {4}
name = "sam"

print("SAM!")
print("Hi " + "Sam")
```

```python {4}
name = "sam"

print("SAM!")
print("Hi Sam")
```

```python {*}
name = "sam"

print(name.upper() + "!")    # SAM!
print("Hi " + name.title())  # Hi Sam
```
````


---
layout: quote
---

# Chaining Methods

<v-click>

You can also chain methods. Each method works on the string the previous one gave back, going left to right:

</v-click>

````md magic-move {lines:true}
```python {*|3}
text = "I like cats"

print(text.replace("cats", "dogs").upper())
```

```python {3}
text = "I like cats"

print("I like cats".replace("cats", "dogs").upper())
```

```python {3}
text = "I like cats"

print("I like dogs".upper())
```

```python {3}
text = "I like cats"

print("I LIKE DOGS")
```

```python {*}
text = "I like cats"

print(text.replace("cats", "dogs").upper())   # I LIKE DOGS
```
````

<v-click>

[QUESTION] Why does `"3" + "4"` give `"34"` but `3 + 4` give `7`?

</v-click>


---
layout: quote
---

# Parentheses Change the Result

<v-click>

The order of operations you already know still applies: `*` comes before `+`, and parentheses go first.

</v-click>

````md magic-move {lines:true}
```python {*|1}
print("ab" + "c" * 3)
print(("ab" + "c") * 3)
```

```python {1}
print("ab" + "ccc")
print(("ab" + "c") * 3)
```

```python {1|2}
print("abccc")
print(("ab" + "c") * 3)
```

```python {2}
print("abccc")
print("abc" * 3)
```

```python {2}
print("abccc")
print("abcabcabc")
```

```python {*}
print("ab" + "c" * 3)     # abccc
print(("ab" + "c") * 3)   # abcabcabc
```
````


---
layout: quote
---

# Parentheses and Methods

<v-click>

A method only works on the string right before the dot, so parentheses can also change which string a method is applied to:

</v-click>

````md magic-move {lines:true}
```python {*|1}
print("a" + "b".upper())
print(("a" + "b").upper())
```

```python {1}
print("a" + "B")
print(("a" + "b").upper())
```

```python {1|2}
print("aB")
print(("a" + "b").upper())
```

```python {2}
print("aB")
print("ab".upper())
```

```python {2}
print("aB")
print("AB")
```

```python {*}
print("a" + "b".upper())     # aB
print(("a" + "b").upper())   # AB
```
````

<v-click>

[PREDICT] What will `"ab" + "cd".upper() * 2` print?

</v-click>


---
layout: quote
---

# Putting It Together

````md magic-move {lines:true}
```python {*|4}
laugh = "ha"
word = "hey"

print(laugh * 3 + " " + word.upper() + "!")
```

```python {4}
laugh = "ha"
word = "hey"

print("ha" * 3 + " " + "hey".upper() + "!")
```

```python {4}
laugh = "ha"
word = "hey"

print("ha" * 3 + " " + "HEY" + "!")
```

```python {4}
laugh = "ha"
word = "hey"

print("hahaha" + " " + "HEY" + "!")
```

```python {4}
laugh = "ha"
word = "hey"

print("hahaha HEY" + "!")
```

```python {4}
laugh = "ha"
word = "hey"

print("hahaha HEY!")
```

```python {*}
laugh = "ha"
word = "hey"

print(laugh * 3 + " " + word.upper() + "!")   # hahaha HEY!
```
````

<v-click>

[MODIFY] Change `laugh` and `word`, and add parentheses somewhere. Predict the output before you run it.

</v-click>


---
layout: quote
---

# String Expression Exercises

Work out what each expression produces on paper, writing out the steps. Then type it into the editor with `print()` to check your answer.

**Join and Repeat:**

````python
a = "ho"
b = "-"
c = "go"
````

1. `a + b + c`
2. `a * 3`
3. `a + b * 2 + c`


---
layout: quote
---

# Join and Repeat: Exercise 1

````md magic-move {lines:true}
```python {*|5}
a = "ho"
b = "-"
c = "go"

a + b + c
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho" + "-" + "go"
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho-go"
```

```python {*}
a = "ho"
b = "-"
c = "go"

a + b + c   # "ho-go"
```
````


---
layout: quote
---

# Join and Repeat: Exercise 2

````md magic-move {lines:true}
```python {*|5}
a = "ho"
b = "-"
c = "go"

a * 3
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho" * 3
```

```python {5}
a = "ho"
b = "-"
c = "go"

"hohoho"
```

```python {*}
a = "ho"
b = "-"
c = "go"

a * 3   # "hohoho"
```
````


---
layout: quote
---

# Join and Repeat: Exercise 3

````md magic-move {lines:true}
```python {*|5}
a = "ho"
b = "-"
c = "go"

a + b * 2 + c
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho" + "-" * 2 + "go"
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho" + "--" + "go"
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho--go"
```

```python {*}
a = "ho"
b = "-"
c = "go"

a + b * 2 + c   # "ho--go"
```
````


---
layout: quote
---

# With Parentheses:

````python
a = "ho"
b = "-"
c = "go"
````

1. `(a + b) * 2`
2. `(a + b) * 2 + c`
3. `a + (b + c) * 2`


---
layout: quote
---

# Parentheses: Exercise 1

````md magic-move {lines:true}
```python {*|5}
a = "ho"
b = "-"
c = "go"

(a + b) * 2
```

```python {5}
a = "ho"
b = "-"
c = "go"

("ho" + "-") * 2
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho-" * 2
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho-ho-"
```

```python {*}
a = "ho"
b = "-"
c = "go"

(a + b) * 2   # "ho-ho-"
```
````


---
layout: quote
---

# Parentheses: Exercise 2

````md magic-move {lines:true}
```python {*|5}
a = "ho"
b = "-"
c = "go"

(a + b) * 2 + c
```

```python {5}
a = "ho"
b = "-"
c = "go"

("ho" + "-") * 2 + "go"
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho-" * 2 + "go"
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho-ho-" + "go"
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho-ho-go"
```

```python {*}
a = "ho"
b = "-"
c = "go"

(a + b) * 2 + c   # "ho-ho-go"
```
````


---
layout: quote
---

# Parentheses: Exercise 3

````md magic-move {lines:true}
```python {*|5}
a = "ho"
b = "-"
c = "go"

a + (b + c) * 2
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho" + ("-" + "go") * 2
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho" + "-go" * 2
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho" + "-go-go"
```

```python {5}
a = "ho"
b = "-"
c = "go"

"ho-go-go"
```

```python {*}
a = "ho"
b = "-"
c = "go"

a + (b + c) * 2   # "ho-go-go"
```
````




---
layout: quote
---

# Methods Exercises:

````python
animal = "cat"
sound = "meow"
````

1. `(animal + sound).upper()`
2. `animal + sound.upper()`
3. `(animal.title() + "!") * 3`


---
layout: quote
---

# Methods: Exercise 1

````md magic-move {lines:true}
```python {*|4}
animal = "cat"
sound = "meow"

(animal + sound).upper()
```

```python {4}
animal = "cat"
sound = "meow"

("cat" + "meow").upper()
```

```python {4}
animal = "cat"
sound = "meow"

"catmeow".upper()
```

```python {4}
animal = "cat"
sound = "meow"

"CATMEOW"
```

```python {*}
animal = "cat"
sound = "meow"

(animal + sound).upper()   # "CATMEOW"
```
````


---
layout: quote
---

# Methods: Exercise 2

````md magic-move {lines:true}
```python {*|4}
animal = "cat"
sound = "meow"

animal + sound.upper()
```

```python {4}
animal = "cat"
sound = "meow"

"cat" + "meow".upper()
```

```python {4}
animal = "cat"
sound = "meow"

"cat" + "MEOW"
```

```python {4}
animal = "cat"
sound = "meow"

"catMEOW"
```

```python {*}
animal = "cat"
sound = "meow"

animal + sound.upper()   # "catMEOW"
```
````


---
layout: quote
---

# Methods: Exercise 3

````md magic-move {lines:true}
```python {*|4}
animal = "cat"
sound = "meow"

(animal.title() + "!") * 3
```

```python {4}
animal = "cat"
sound = "meow"

("cat".title() + "!") * 3
```

```python {4}
animal = "cat"
sound = "meow"

("Cat" + "!") * 3
```

```python {4}
animal = "cat"
sound = "meow"

"Cat!" * 3
```

```python {4}
animal = "cat"
sound = "meow"

"Cat!Cat!Cat!"
```

```python {*}
animal = "cat"
sound = "meow"

(animal.title() + "!") * 3   # "Cat!Cat!Cat!"
```
````


---
layout: quote
---

# Challenge Exercises:

````python
phrase = "I like cats"
name = "ada"
dash = "-"
````

1. `phrase.replace("cats", "dogs").upper()`
2. `name.title() + " " + name.upper() * 2`
3. `(name + dash).upper() * 3 + "GO"`
4. `phrase.replace("like", "love").replace("cats", name.title())`


---
layout: quote
---

# Challenge: Exercise 1

````md magic-move {lines:true}
```python {*|5}
phrase = "I like cats"
name = "ada"
dash = "-"

phrase.replace("cats", "dogs").upper()
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"I like cats".replace("cats", "dogs").upper()
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"I like dogs".upper()
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"I LIKE DOGS"
```

```python {*}
phrase = "I like cats"
name = "ada"
dash = "-"

phrase.replace("cats", "dogs").upper()   # "I LIKE DOGS"
```
````


---
layout: quote
---

# Challenge: Exercise 2

````md magic-move {lines:true}
```python {*|5}
phrase = "I like cats"
name = "ada"
dash = "-"

name.title() + " " + name.upper() * 2
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"ada".title() + " " + "ada".upper() * 2
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"Ada" + " " + "ada".upper() * 2
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"Ada" + " " + "ADA" * 2
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"Ada" + " " + "ADAADA"
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"Ada ADAADA"
```

```python {*}
phrase = "I like cats"
name = "ada"
dash = "-"

name.title() + " " + name.upper() * 2   # "Ada ADAADA"
```
````


---
layout: quote
---

# Challenge: Exercise 3

````md magic-move {lines:true}
```python {*|5}
phrase = "I like cats"
name = "ada"
dash = "-"

(name + dash).upper() * 3 + "GO"
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

("ada" + "-").upper() * 3 + "GO"
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"ada-".upper() * 3 + "GO"
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"ADA-" * 3 + "GO"
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"ADA-ADA-ADA-" + "GO"
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"ADA-ADA-ADA-GO"
```

```python {*}
phrase = "I like cats"
name = "ada"
dash = "-"

(name + dash).upper() * 3 + "GO"   # "ADA-ADA-ADA-GO"
```
````


---
layout: quote
---

# Challenge: Exercise 4

````md magic-move {lines:true}
```python {*|5}
phrase = "I like cats"
name = "ada"
dash = "-"

phrase.replace("like", "love").replace("cats", name.title())
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"I like cats".replace("like", "love").replace("cats", "ada".title())
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"I like cats".replace("like", "love").replace("cats", "Ada")
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"I love cats".replace("cats", "Ada")
```

```python {5}
phrase = "I like cats"
name = "ada"
dash = "-"

"I love Ada"
```

```python {*}
phrase = "I like cats"
name = "ada"
dash = "-"

phrase.replace("like", "love").replace("cats", name.title())   # "I love Ada"
```
````


---
layout: quote
---

# Write the Expression

Write one expression (inside `print()`) that produces the expected output. The variables are already set up for you.


---
layout: quote
---

# Example 1: Laugh Generator

````python
laugh = "ha"
````

Expected output:

````
HAHAHA!
````

<v-click>

````python
print(laugh.upper() * 3 + "!")   # HAHAHA!
````

</v-click>


---
layout: quote
---

# Example 2: Email Address Builder

````python
first = "Maya"
last = "Khan"
domain = "school.org"
````

Expected output:

````
maya.khan@school.org
````

<v-click>

````python
print(first.lower() + "." + last.lower() + "@" + domain)   # maya.khan@school.org
````

</v-click>


---
layout: quote
---

# Example 3: Menu Banner

````python
title = "menu"
````

Expected output:

````
===== MENU =====
````

<v-click>

````python
print("=" * 5 + " " + title.upper() + " " + "=" * 5)   # ===== MENU =====
````

</v-click>


---
layout: quote
---

# Example 4: Echo

````python
word = "hello"
````

Expected output:

````
hello, hello, hello
````

<v-click>

````python
print((word + ", ") * 2 + word)   # hello, hello, hello
````

</v-click>

<v-click>

[MODIFY] Change the variables in each example to your own values. Does your expression still work?

</v-click>