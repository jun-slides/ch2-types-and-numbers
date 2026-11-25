---
layout: quote
---

# Exercise: Add two digits

Asks you to type a 2 digit number, and outputs the sum of it’s digits so 45 → 9
    
<div v-click>
  <iframe
    v-if="$clicks >= 1"
    src="https://trinket.strivemath.org/embed/python3/2681e9258808?outputOnly=true&runOption=run&start=result"
    class="w-full h-80 rounded-lg border border-gray-500/40 mt-6"
  ></iframe>
</div>


---
layout: quote
---


# Instructions
    
Write a program that adds the digits in a 2 digit number.
<br>
e.g. if the input was 35, then the output should be 3 + 5 = 8

**Example 1**
- Input: `39`
- Output: `12`

**Example 2**
- Input: `43`
- Output: `7`

---
layout: quote
---

    
# Starting code
    
```python
# take input for a 2 digit number
two_digit_number = input("Type a 2 digit number: ")

# extract each digit from two_digit_number 

# convert each digit to an integer

# add up the digits as integers

# print the result.
```
    
---
layout: quote
---
    
# Solution
    
```python
two_digit_number = input("Type a 2 digit number: ")

first_digit = int(two_digit_number[0])
second_digit = int(two_digit_number[1])

# Add the two integers together
digit_sum = first_digit + second_digit

print(digit_sum)
```
    

[TRY IT] Type 23 and see the output.