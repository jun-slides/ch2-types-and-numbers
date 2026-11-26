---
layout: quote
---


# Getting Numbers from Input

`input()` always returns text. To do math, convert it:



```python {*|1|2|*} {lines:true} 
age = input("How old are you? ")
print(age + 10)  # This will ERROR!
```

<v-click>

[PREDICT] Why does this fail?

</v-click>


---
layout: quote
---


# **Fix it with `int()` or `float()`:**


<v-clicks>

1. using int()

```python
age = int(input("How old are you? "))
print(age + 10)  # Now it works!

```

2. using float()

```python
price = float(input("Enter price: "))
print(price * 2)

```

[QUESTION] When would you use `int()` vs `float()`?

</v-clicks>



---
layout: quote
---

# Input Type Conversion animation 1


````md magic-move {lines:true}
```python {*|1}
age = input("How old are you? ")
age = int(age)
print(age + 10) 
```

```python {1|2}
age = '25'
age = int(age)
print(age + 10) 
```

```python {2}
age = '25'
age = int('25')
print(age + 10) 
```

```python {2|3}
age = '25'
age = 25
print(age + 10) 
```


```python {3}
age = '25'
age = 25
print(25 + 10) 
```



```python {3}
age = '25'
age = 25
print(35) 
```

```python
age = input("How old are you? ")
age = int(age)
print(age + 10) 
```

````



---
layout: quote
---

# Input Type Conversion animation 2


````md magic-move {lines:true}
```python {*|1}
age = int(input("How old are you? "))
print(age + 10) 
```

```python {1}
age = int('25')
print(age + 10) 
```

```python {1|2}
age = 25
print(age + 10) 
```


```python {2}
age = 25
print(25 + 10) 
```

```python {2}
age = 25
print(35) 
```

```python
age = int(input("How old are you? "))
print(age + 10) 
```
````