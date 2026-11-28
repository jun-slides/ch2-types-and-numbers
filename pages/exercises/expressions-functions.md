---
layout: quote
---

# Expressions with Variables and Function Calls

<v-clicks>

So far every expression you've solved was made of numbers and operators.

But an expression is really *anything Python can work out to a single value*.

Besides numbers, an expression can also contain **variables** and **function calls**.

</v-clicks>

<table v-click="4">
  <thead>
    <tr v-click><th>Ingredient</th><th>Example</th><th>Python replaces it with</th></tr>
  </thead>
  <tbody>
    <tr v-click><td>Number</td><td><code>5</code></td><td>itself</td></tr>
    <tr v-click><td>Variable</td><td><code>price</code></td><td>the value stored in the variable</td></tr>
    <tr v-click><td>Function call</td><td><code>len("Hi")</code></td><td>the value the function gives back</td></tr>
    <tr v-click><td>Operator</td><td><code>+</code> <code>-</code> <code>*</code> <code>/</code></td><td>(combines the values around it)</td></tr>
  </tbody>
</table>


---
layout: quote
---

# Variables in Expressions

<v-click>

When Python sees a variable inside an expression, it swaps the variable for the value stored in it, then does the math as usual:

</v-click>



````md magic-move {lines:true}
```python {*|4}
price = 20
quantity = 3

print(price * quantity)
```

```python {4}
price = 20
quantity = 3

print(20 * 3)
```

```python {4}
price = 20
quantity = 3

print(60)
```

```python {*}
price = 20
quantity = 3

print(price * quantity)   # 60
```
````


---
layout: quote
---

# The Right Side of = Is an Expression

<v-click>

The right side of an `=` is also an expression. Python works it out first, then stores the answer in the variable on the left:

</v-click>

````md magic-move {lines:true}
```python {*|4}
price = 20
quantity = 3

total = price * quantity - 5   
print(total)
```

```python {4}
price = 20
quantity = 3

total = 20 * 3 - 5   
print(total)
```

```python {4}
price = 20
quantity = 3

total = 60 - 5   
print(total)
```

```python {4|5}
price = 20
quantity = 3

total = 55  
print(total)
```

```python {5}
price = 20
quantity = 3

total = 55  
print(55)
```

```python {*}
price = 20
quantity = 3

total = price * quantity - 5   
print(total)                   # 55
```
````

<v-click>

[QUESTION] In `total = price * quantity - 5`, which part is the expression?

</v-click>


---
layout: quote
---

# Function Calls in Expressions

<v-click>

A function call is an expression too. When the function finishes, it **gives back a value**, and that value takes the place of the call:

</v-click>

````md magic-move {lines:true}
```python {*|1}
print(len("Python"))
print(len("Python") * 2)
```

```python {1|2}
print(6)
print(len("Python") * 2)
```

```python {2}
print(6)
print(6 * 2)
```

```python {2}
print(6)
print(12)
```

```python {*}
print(len("Python"))       # 6
print(len("Python") * 2)   # 12
```
````

<v-click>

So anywhere you could write the number `6`, you can write `len("Python")` instead.

</v-click>


---
layout: quote
---

# Analogy: The Vending Machine

<v-click>

A function call is like a vending machine. You put something in (the **argument**), something comes out (the **returned value**), and what comes out takes the place of the whole call.

</v-click>

<v-click>

Here are a few built-in functions you can use inside expressions (we'll look at some of them in more detail later):

</v-click>

<table v-click="3">
  <thead>
    <tr v-click><th>Function call</th><th>Gives back</th><th>Result</th></tr>
  </thead>
  <tbody>
    <tr v-click><td><code>len("Hello")</code></td><td>number of characters</td><td><code>5</code></td></tr>
    <tr v-click><td><code>abs(-7)</code></td><td>the number without its minus sign</td><td><code>7</code></td></tr>
    <tr v-click><td><code>max(4, 9, 2)</code></td><td>the biggest value</td><td><code>9</code></td></tr>
    <tr v-click><td><code>min(4, 9, 2)</code></td><td>the smallest value</td><td><code>2</code></td></tr>
  </tbody>
</table>

<v-click>

[TRY IT] Run each of these in the editor and check the results match the table.

</v-click>


---
layout: quote
---

# Arguments Can Be Expressions Too

<v-click>

The argument you put into a function can be an expression too. Python solves the inside first, then runs the function:

</v-click>

````md magic-move {lines:true}
```python {*}
print(abs(3 - 10))
```

```python {*}
print(abs(-7))
```

```python {*}
print(7)
```

```python {*}
print(abs(3 - 10))   # 7
```
````

<v-click>

[PREDICT] What will `abs(3 - 10) * 2` print?

</v-click>


---
layout: quote
---

# Putting It Together

<v-click>

Our order of operations gets one new step at the very start.

</v-click>

<v-click>

Python first swaps in the variables and runs the function calls (inside-out), and then follows PEMDAS as before.

</v-click>

````md magic-move {lines:true}
```python {*|4}
name = "Alex"
age = 12

print(len(name) + age * 2)
```

```python {4}
name = "Alex"
age = 12

print(len("Alex") + 12 * 2)
```

```python {4}
name = "Alex"
age = 12

print(4 + 12 * 2)
```

```python {4}
name = "Alex"
age = 12

print(4 + 24)
```

```python {4}
name = "Alex"
age = 12

print(28)
```

```python {*}
name = "Alex"
age = 12

print(len(name) + age * 2)   # 28
```
````

<v-click>

Even `print()` is a function call. The expression inside its parentheses is solved first, and then `print()` displays the result.

</v-click>

<v-click>

[MODIFY] Change `name` to your own name and `age` to your age. Predict the output before you run it.

</v-click>


---
layout: quote
---

# Expression Exercises: Variables and Function Calls

Solve these exercises by hand. Then type the code into the editor to check your answer.


```python
score = 12
bonus = 3
lives = 4
```

1. `score + bonus * 2`
2. `(score + bonus) * 2`
3. `score / lives + bonus`



---
layout: quote
---

# Variables: Exercise 1

````md magic-move {lines:true}
```python {*|5}
score = 12
bonus = 3
lives = 4

score + bonus * 2
```

```python {5}
score = 12
bonus = 3
lives = 4

12 + 3 * 2
```

```python {5}
score = 12
bonus = 3
lives = 4

12 + 6
```

```python {5}
score = 12
bonus = 3
lives = 4

18
```

```python {*}
score = 12
bonus = 3
lives = 4

score + bonus * 2   # 18
```
````




---
layout: quote
---

# Variables: Exercise 2

````md magic-move {lines:true}
```python {*|5}
score = 12
bonus = 3
lives = 4

(score + bonus) * 2
```

```python {5}
score = 12
bonus = 3
lives = 4

(12 + 3) * 2
```

```python {5}
score = 12
bonus = 3
lives = 4

15 * 2
```

```python {5}
score = 12
bonus = 3
lives = 4

30
```

```python {*}
score = 12
bonus = 3
lives = 4

(score + bonus) * 2   # 30
```
````



---
layout: quote
---

# Variables: Exercise 3

````md magic-move {lines:true}
```python {*|5}
score = 12
bonus = 3
lives = 4

score / lives + bonus
```

```python {5}
score = 12
bonus = 3
lives = 4

12 / 4 + 3
```

```python {5}
score = 12
bonus = 3
lives = 4

3.0 + 3
```

```python {5}
score = 12
bonus = 3
lives = 4

6.0
```

```python {*}
score = 12
bonus = 3
lives = 4

score / lives + bonus   # 6.0
```
````

    
---
layout: quote
---

# Expressions with Function Calls:

1. `len("Python") + 4`
2. `abs(5 - 12) * 2`
3. `max(3, 8, 5) - min(3, 8, 5)`

---
layout: quote
---

# Function Calls: Exercise 1

````md magic-move {lines:true}
```python
len("Python") + 4
```

```python {1}
6 + 4
```

```python {1}
10
```

```python {*}
len("Python") + 4   # 10
```
````


---
layout: quote
---

# Function Calls: Exercise 2

````md magic-move {lines:true}
```python 
abs(5 - 12) * 2
```

```python {1}
abs(-7) * 2
```

```python {1}
7 * 2
```

```python {1}
14
```

```python {*}
abs(5 - 12) * 2   # 14
```
````


---
layout: quote
---

# Function Calls: Exercise 3

````md magic-move {lines:true}
```python
max(3, 8, 5) - min(3, 8, 5)
```

```python {1}
8 - min(3, 8, 5)
```

```python {1}
8 - 3
```

```python {1}
5
```

```python {*}
max(3, 8, 5) - min(3, 8, 5)   # 5
```
````

<v-click>

[QUESTION] What's the difference between `max(3, 8, 5)` and `max(3 + 8 + 5)` ?

</v-click>


---
layout: quote
---

# Variables and Function Calls Together:

```python
word = "banana"
price = 4
quantity = 3
```

1. `len(word) * 2`
2. `price * quantity + len(word)`
3. `max(price, quantity) ** 2 - min(price, quantity)`


---
layout: quote
---


# Together: Exercise 1

````md magic-move {lines:true}
```python {*|5}
word = "banana"
price = 4
quantity = 3

len(word) * 2
```

```python {5}
word = "banana"
price = 4
quantity = 3

len("banana") * 2
```

```python {5}
word = "banana"
price = 4
quantity = 3

6 * 2
```

```python {5}
word = "banana"
price = 4
quantity = 3

12
```

```python {*}
word = "banana"
price = 4
quantity = 3

len(word) * 2   # 12
```
````


---
layout: quote
---

# Together: Exercise 2

````md magic-move {lines:true}
```python {*|5}
word = "banana"
price = 4
quantity = 3

price * quantity + len(word)
```

```python {5}
word = "banana"
price = 4
quantity = 3

4 * 3 + len("banana")
```

```python {5}
word = "banana"
price = 4
quantity = 3

4 * 3 + 6
```

```python {5}
word = "banana"
price = 4
quantity = 3

12 + 6
```

```python {5}
word = "banana"
price = 4
quantity = 3

18
```

```python {*}
word = "banana"
price = 4
quantity = 3

price * quantity + len(word)   # 18
```
````


---
layout: quote
---

# Together: Exercise 3

````md magic-move {lines:true}
```python {*|5}
word = "banana"
price = 4
quantity = 3

max(price, quantity) ** 2 - min(price, quantity)
```

```python {5}
word = "banana"
price = 4
quantity = 3

max(4, 3) ** 2 - min(4, 3)
```

```python {5}
word = "banana"
price = 4
quantity = 3

4 ** 2 - min(4, 3)
```

```python {5}
word = "banana"
price = 4
quantity = 3

4 ** 2 - 3
```

```python {5}
word = "banana"
price = 4
quantity = 3

16 - 3
```

```python {5}
word = "banana"
price = 4
quantity = 3

13
```

```python {*}
word = "banana"
price = 4
quantity = 3

max(price, quantity) ** 2 - min(price, quantity)   # 13
```
````
    
---
layout: quote
---

# Challenge Exercises:

```python
a = 7
b = 10
name = "Alex"
```

1. `abs(a - b) * len(name)`
2. `max(a, b) // 3 + len(name) ** 2`
3. `(len(name) + a) * 2 - abs(a - b) ** 2`
4. `min(a, b) + max(a * 2, b + 3) / 2`



---
layout: quote
---

# Challenge: Exercise 1

````md magic-move {lines:true}
```python {*|5}
a = 7
b = 10
name = "Alex"

abs(a - b) * len(name)
```

```python {5}
a = 7
b = 10
name = "Alex"

abs(7 - 10) * len("Alex")
```

```python {5}
a = 7
b = 10
name = "Alex"

abs(-3) * len("Alex")
```

```python {5}
a = 7
b = 10
name = "Alex"

3 * len("Alex")
```

```python {5}
a = 7
b = 10
name = "Alex"

3 * 4
```

```python {5}
a = 7
b = 10
name = "Alex"

12
```

```python {*}
a = 7
b = 10
name = "Alex"

abs(a - b) * len(name)   # 12
```
````


---
layout: quote
---

# Challenge: Exercise 2

````md magic-move {lines:true}
```python {*|5}
a = 7
b = 10
name = "Alex"

max(a, b) // 3 + len(name) ** 2
```

```python {5}
a = 7
b = 10
name = "Alex"

max(7, 10) // 3 + len("Alex") ** 2
```

```python {5}
a = 7
b = 10
name = "Alex"

10 // 3 + len("Alex") ** 2
```

```python {5}
a = 7
b = 10
name = "Alex"

10 // 3 + 4 ** 2
```

```python {5}
a = 7
b = 10
name = "Alex"

3 + 16
```

```python {5}
a = 7
b = 10
name = "Alex"

19
```

```python {*}
a = 7
b = 10
name = "Alex"

max(a, b) // 3 + len(name) ** 2   # 19
```
````


---
layout: quote
---

# Challenge: Exercise 3

````md magic-move {lines:true}
```python {*|5}
a = 7
b = 10
name = "Alex"

(len(name) + a) * 2 - abs(a - b) ** 2
```

```python {5}
a = 7
b = 10
name = "Alex"

(len("Alex") + 7) * 2 - abs(7 - 10) ** 2
```

```python {5}
a = 7
b = 10
name = "Alex"

(4 + 7) * 2 - abs(7 - 10) ** 2
```

```python {5}
a = 7
b = 10
name = "Alex"

(4 + 7) * 2 - abs(-3) ** 2
```

```python {5}
a = 7
b = 10
name = "Alex"

(4 + 7) * 2 - 3 ** 2
```

```python {5}
a = 7
b = 10
name = "Alex"

11 * 2 - 3 ** 2
```

```python {5}
a = 7
b = 10
name = "Alex"

22 - 9
```

```python {5}
a = 7
b = 10
name = "Alex"

13
```

```python {*}
a = 7
b = 10
name = "Alex"

(len(name) + a) * 2 - abs(a - b) ** 2    # 13
```
````


---
layout: quote
---

# Challenge: Exercise 4

````md magic-move {lines:true}
```python {*|5}
a = 7
b = 10
name = "Alex"

min(a, b) + max(a * 2, b + 3) / 2
```

```python {5}
a = 7
b = 10
name = "Alex"

min(7, 10) + max(7 * 2, 10 + 3) / 2
```

```python {5}
a = 7
b = 10
name = "Alex"

7 + max(7 * 2, 10 + 3) / 2
```

```python {5}
a = 7
b = 10
name = "Alex"

7 + max(14, 13) / 2
```

```python {5}
a = 7
b = 10
name = "Alex"

7 + 14 / 2
```

```python {5}
a = 7
b = 10
name = "Alex"

7 + 7.0
```

```python {5}
a = 7
b = 10
name = "Alex"

14.0
```

```python {*}
a = 7
b = 10
name = "Alex"

min(a, b) + max(a * 2, b + 3) / 2    # 14.0
```
````
