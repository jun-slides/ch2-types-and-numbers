---
layout: quote
---

# Exercise Fahrenheit to Celsius

Convert Temperature given in Fahrenheit to Celsius using formula:  $C = {5\above{1pt} 9} * (F - 32)$


<div v-click>
  <iframe
    v-if="$clicks >= 1"
    src="https://trinket.strivemath.org/embed/python3/a37248776972?outputOnly=true&runOption=run&start=result"
    class="w-full h-80 rounded-lg border border-gray-500/40 mt-6"
  ></iframe>
</div>


<v-click>

[TRY IT] Convert 50°F to Celsius.    

</v-click>

---
layout: quote
---


# Instructions
1. Ask for temperature in Fahrenheit
2. Convert using formula:  $C = {5\above{1pt} 9} * (F - 32)$
3. Print the result



---
layout: quote
---


# Starting code:

```python
print("=== Temperature Converter ===")
print()

# Step 1: Ask for temperature in Fahrenheit (float)

# Step 2: Convert using formula

# Step 3: Print the result

```

---
layout: quote
---

# Solution

```python
print("=== Temperature Converter ===")
print()
fahrenheit = float(input("Enter temperature in Fahrenheit: "))

celsius = 5/9 * (fahrenheit - 32)

print(f"{fahrenheit}°F = {celsius:.1f}°C")

```
    
