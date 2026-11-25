---
layout: quote
---


# Exercise Celsius to Fahrenheit

Ask for temperature in Celsius and convert it into Fahrenheit. using formula:  $F = {9\above{1pt} 5}C + 32$

<div v-click>
  <iframe
    v-if="$clicks >= 1"
    src="https://trinket.strivemath.org/embed/python3/728f2d06d526?outputOnly=true&runOption=run&start=result"
    class="w-full h-80 rounded-lg border border-gray-500/40 mt-6"
  ></iframe>
</div>


<v-click>

[TRY IT] Convert 25°C to Fahrenheit. Then try 100°C (boiling water) and 0°C (freezing point).

</v-click>

---
layout: quote
---

# Instructions

1. Ask for temperature in Celsius
2. Convert using formula:  $F = {9\above{1pt} 5}C + 32$
3. Print the result


---
layout: quote
---

# Starting code
    
```python
print("=== Temperature Converter ===")
print()

# Step 1: Ask for temperature in Celsius (float)

# Step 2: Convert using formula

# Step 3: Print the result

```


---
layout: quote
---

# Solution:

```python
print("=== Temperature Converter ===")
print()
celsius = float(input("Enter temperature in Celsius: "))

fahrenheit = (9/5 * celsius) + 32

print(f"{celsius}°C = {fahrenheit:.1f}°F")

```

