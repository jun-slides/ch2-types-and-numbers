---
layout: quote
---


# Type Conversion

Type conversion means converting the type of a value into another type, ie `'10'` -> `10`

<v-click>

You can convert between types using these functions:

| Function | Converts to |
| --- | --- |
| `str()` | String |
| `int()` | Integer |
| `float()` | Float |

</v-click>

---
layout: quote
---


# Type Conversion Examples

<v-click>

**String to Integer**
```python
age_str = "25"
age_int = int(age_str)
print(age_int + 5)   # 30
```

</v-click>


<v-click>


**Integer to String**
```python
num = 100
text = str(num)
print("Score: " + text)   # Score: 100
```

</v-click>

<v-click>


**String to Float**
```python
# String to Float
price = float("19.99")
print(price * 2)   # 39.98
```

</v-click>


---
layout: quote
---


# Type Conversion Animation

**String to Integer**

````md magic-move {lines:true}
```python {*|1|2}
age_str = "25"
age_int = int(age_str)
print(age_int + 5)   # 30
```

```python {2}
age_str = "25"
age_int = int("25")
print(age_int + 5)   # 30
```


```python {2|3}
age_str = "25"
age_int = 25
print(age_int + 5)   # 30
```

```python {3}
age_str = "25"
age_int = 25
print(25 + 5)   # 30
```

```python {3|*}
age_str = "25"
age_int = 25
print(30)   # 30
```

```python
age_str = "25"
age_int = int(age_str)
print(age_int + 5)   # 30
```

````

---
layout: quote
---


# But why bother with the conversion?

In real life you won’t be given the type of your choice so you need to be able to change the data in your desired type

---
layout: quote
---

# Type Conversion: Practical Example
Adding `10` to `"$150"` to get `"$160"`

````md magic-move {lines:true}
```python {*|1-4}
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

```python {1-4|6-7}
# I want to add 10 to '$150'

price = '$150'
print('Original price: $150')

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


```python {6-7|9-10}
# I want to add 10 to '$150'

price = '$150'
print('Original price: $150')

# first remove $ so the values becomes '150'
remove_dollar = '150'

# then convert it to an int so it becomes 150
num_price = int(remove_dollar)

# add 10 to the 'clean' price
new_price = num_price + 10

# convert back to string and add the removed dollar sign
# so we started from '$150' and ended with '$160'
price = '$' + str(new_price)
print(f'New price: {price}')
```

```python {9-10}
# I want to add 10 to '$150'

price = '$150'
print('Original price: $150')

# first remove $ so the values becomes '150'
remove_dollar = '150'

# then convert it to an int so it becomes 150
num_price = int('150')

# add 10 to the 'clean' price
new_price = num_price + 10

# convert back to string and add the removed dollar sign
# so we started from '$150' and ended with '$160'
price = '$' + str(new_price)
print(f'New price: {price}')
```

```python {9-10|12-13}
# I want to add 10 to '$150'

price = '$150'
print('Original price: $150')

# first remove $ so the values becomes '150'
remove_dollar = '150'

# then convert it to an int so it becomes 150
num_price = 150

# add 10 to the 'clean' price
new_price = num_price + 10

# convert back to string and add the removed dollar sign
# so we started from '$150' and ended with '$160'
price = '$' + str(new_price)
print(f'New price: {price}')
```

```python {12-13}
# I want to add 10 to '$150'

price = '$150'
print('Original price: $150')

# first remove $ so the values becomes '150'
remove_dollar = '150'

# then convert it to an int so it becomes 150
num_price = 150

# add 10 to the 'clean' price
new_price = 150 + 10

# convert back to string and add the removed dollar sign
# so we started from '$150' and ended with '$160'
price = '$' + str(new_price)
print(f'New price: {price}')
```


```python {12-13|15-18}
# I want to add 10 to '$150'

price = '$150'
print('Original price: $150')

# first remove $ so the values becomes '150'
remove_dollar = '150'

# then convert it to an int so it becomes 150
num_price = 150

# add 10 to the 'clean' price
new_price = 160

# convert back to string and add the removed dollar sign
# so we started from '$150' and ended with '$160'
price = '$' + str(new_price)
print(f'New price: {price}')
```

```python {15-18}
# I want to add 10 to '$150'

price = '$150'
print('Original price: $150')

# first remove $ so the values becomes '150'
remove_dollar = '150'

# then convert it to an int so it becomes 150
num_price = 150

# add 10 to the 'clean' price
new_price = 160

# convert back to string and add the removed dollar sign
# so we started from '$150' and ended with '$160'
price = '$' + str(160)
print(f'New price: {price}')
```

```python {15-18}
# I want to add 10 to '$150'

price = '$150'
print('Original price: $150')

# first remove $ so the values becomes '150'
remove_dollar = '150'

# then convert it to an int so it becomes 150
num_price = 150

# add 10 to the 'clean' price
new_price = 160

# convert back to string and add the removed dollar sign
# so we started from '$150' and ended with '$160'
price = '$' + '160'
print(f'New price: {price}')
```


```python {15-18}
# I want to add 10 to '$150'

price = '$150'
print('Original price: $150')

# first remove $ so the values becomes '150'
remove_dollar = '150'

# then convert it to an int so it becomes 150
num_price = 150

# add 10 to the 'clean' price
new_price = 160

# convert back to string and add the removed dollar sign
# so we started from '$150' and ended with '$160'
price = '$160'
print(f'New price: {price}')
```

```python {15-18}
# I want to add 10 to '$150'

price = '$150'
print('Original price: $150')

# first remove $ so the values becomes '150'
remove_dollar = '150'

# then convert it to an int so it becomes 150
num_price = 150

# add 10 to the 'clean' price
new_price = 160

# convert back to string and add the removed dollar sign
# so we started from '$150' and ended with '$160'
price = '$160'
print('New price: $160')
```


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

````
