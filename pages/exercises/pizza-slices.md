---
layout: quote
---

# Practice Challenge: Slices to Pizzas

Calculates how many pizzas to order for a party.

<div v-click>
  <iframe
    v-if="$clicks >= 1"
    src="https://trinket.strivemath.org/embed/python3/150184f698a1?outputOnly=true&runOption=run&start=result"
    class="w-full h-80 rounded-lg border border-gray-500/40 mt-6"
  ></iframe>
</div>



---
layout: quote
---


# Starting code:
    
```python
# Step 1: Ask how many people are coming (int)

# Step 2: Ask how many slices each person eats (int)

# Step 3: Calculate total slices needed

# Step 4: Each pizza has 8 slices - calculate pizzas needed (round up!)

# Step 5: Print the party plan with formatting

```

---
layout: quote
---


    
# Solution:
    
```python
import math

# ask for the input
people = int(input("How many people? "))
slices_per_person = int(input("Slices per person? "))

# do the math
total_slices = people * slices_per_person
full_pizzas = total_slices // 8
slices = total_slices % 8
pizzas_needed = math.ceil(total_slices / 8)

# display the results
print()
print("=== PIZZA PARTY PLAN ===")
print(f"Guests: {people}")
print(f"Total slices needed: {total_slices}")
print(f"That means {full_pizzas} full pizza(s) and extra {slices} slice(s)")
print(f"Pizzas to order: {pizzas_needed}")
```
    
