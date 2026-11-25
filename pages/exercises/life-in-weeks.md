---
layout: quote
---

# Exercise: Life in weeks

Create a program that tells us how many weeks we have left to live, if we live until 90 years old.

<div v-click>
  <iframe
    v-if="$clicks >= 1"
    src="https://trinket.strivemath.org/embed/python3/5b51e38deddc?outputOnly=true&runOption=run&start=result"
    class="w-full h-80 rounded-lg border border-gray-500/40 mt-6"
  ></iframe>
</div>


[TRY IT] Try it with your age. How does it make you feel?



---
layout: quote
---

    
# Instructions
    
1. Ask for the age
2. Take the difference with 90
3. Covert to weeks
4. Print the result


Example 

- Input `56`
- Output:

```
You have 1768 weeks left.
Use them wisely 😉.
```


---
layout: quote
---

    
# Starting code
    
```python
# take age as input
age = input("Enter your age: ")

# convert age to integer

# calculate remaining years (difference between 90 and age)

# convert remaining years into weeks

# print the result
```

---
layout: quote
---

    
# Solution

```python
age = input("Enter your age: ")
print()

years = 90 - int(age)
weeks = years * 52

print(f"You have {weeks} weeks left.")
print("Use them wisely 😉.")
```
    
[MODIFY] Add remaining days, hours, minutes.