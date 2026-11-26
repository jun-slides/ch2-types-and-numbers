---
layout: quote
---


# Expression Exercises

Solve these exercises using pen and paper and then type the code into an editor to check if your answer matches.



---
layout: quote
---

# Basic Expressions:

1. `3 + 4 * 2`
2. `10 / 2 * 3`
3. `7 + 8 / 3`



---
layout: quote
---

# Basic Expressions Solution:


````md magic-move {lines:true}
```python {1}
3 + 4 * 2
10 / 2 * 3
7 + 8 / 3
```

```python {1}
3 + 8
10 / 2 * 3
7 + 8 / 3
```

```python {1|2}
11
10 / 2 * 3
7 + 8 / 3
```

```python {2}
11
5.0 * 3
7 + 8 / 3
```

```python {2|3}
11
15.0
7 + 8 / 3
```

```python {3}
11
15.0
7 + 2.6666
```

```python {3|*}
11
15.0
9.6666
```


```python 
3 + 4 * 2     # output: 11
10 / 2 * 3    # output: 15.0
7 + 8 / 3     # output: 9.6666
```

````


---
layout: quote
---


# Expressions with Parentheses:

1. `(3 + 4) * 2`
2. `(10 / (2 * 5)) + 3`
3. `7 + (6 / (3 + 3))`


---
layout: quote
---

# Solution Expressions with Parentheses 

````md magic-move {lines:true}
```python {*|1}
(3 + 4) * 2
(10 / (2 * 5)) + 3
7 + (6 / (3 + 3))
```

```python {1}
7 * 2
(10 / (2 * 5)) + 3
7 + (6 / (3 + 3))
```

```python {1|2}
14
(10 / (2 * 5)) + 3
7 + (6 / (3 + 3))
```

```python {2}
14
(10 / 10) + 3
7 + (6 / (3 + 3))
```

```python {2}
14
1.0 + 3
7 + (6 / (3 + 3))
```

```python {2|3}
14
4.0
7 + (6 / (3 + 3))
```


```python {3}
14
4.0
7 + (6 / 6)
```


```python {3}
14
4.0
7 + 1
```

```python {3|*}
14
4.0
8
```


```python 
(3 + 4) * 2           # Output: 14
(10 / (2 * 5)) + 3    # Output: 4.0
7 + (6 / (3 + 3))     # Output: 8
```
````


---
layout: quote
---



# Expressions with Exponents:

1. `2 ** 3 * 4`
2. `3 + 2 ** 2 * 5`
3. `(2 + 3) ** 2`


---
layout: quote
---


# Solution Expressions with Exponents:
Todo animate these

```python
2 ** 3 * 4
3 + 2 ** 2 * 5
(2 + 3) ** 2
```

---
layout: quote
---


# Challenge Exercises:

1. `5 + 3 * (8 - 4) / 2`
2. `(12 / 4) + (3 * 2) - 5`
3. `18 - 3 ** 2 + 4 * (6 / 2)`
4. `100 / (5 * 2) + 3 ** 2 - 7`


---
layout: quote
---


# Solution Challenge Exercises:
TODO animate these

```python
5 + 3 * (8 - 4) / 2
(12 / 4) + (3 * 2) - 5
18 - 3 ** 2 + 4 * (6 / 2)
100 / (5 * 2) + 3 ** 2 - 7

```




---
layout: quote
---

# Write expressions for the following problems


<v-clicks>

**Example 1: Age Calculator**

Calculate age in months for someone who is 25 years old

```python
25 * 12     # Output: 300
```
    

**Example 2: Circle Area**

Calculate area of a circle with radius 5 (using 3.14 for pi)r
Formula for circle's area is $\pi r ^ 2$


```python
3.14 * 5 ** 2  # Output: 78.5
```
    
</v-clicks>    


---
layout: quote
---


**Example 3: Weekly Savings**

<v-clicks>


If you save $15 per day, how much in a week?


```python
15 * 7    # Output: 105
```
    

**Exercise 4: Test Score Average**

Calculate the average of these test scores: 85, 92, 78, 90, 88

    
```python
(85 + 92 + 78 + 90 + 88) / 5
```

</v-clicks>


---
layout: quote
---


# More exercises
    

1. Write the code to find the number of times 5 goes evenly into 18.

2. Write the code to find the remainder when dividing 20 by 3.

3. Write the code to raise 8 to the power of 3.

4. Determine what the code will output before running it.
    1. `(10 + 3) * 2 - (10 % 3) + 10 // 3`
    2. `2 + 6 * 2 ** 2 // 4 - 3`
    3. `15 // 4 + 6 * 2 - 9 % 4`

