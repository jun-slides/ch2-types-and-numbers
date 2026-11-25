---
layout: quote
---

# Exercise: Tip Calculator

Calculates the tip and total amount based on bill and tip percentage entered by user.
    
<div v-click>
  <iframe
    v-if="$clicks >= 1"
    src="https://trinket.strivemath.org/embed/python3/b2d2b9cb9ed1?outputOnly=true&runOption=run&start=result"
    class="w-full h-80 rounded-lg border border-gray-500/40 mt-6"
  ></iframe>
</div>


---
layout: quote
---
  
# Instructions
    1. Ask for the bill amount
    2. Ask for the tip percentage
    3. Calculate the tip amount
    4. Calculate the total (bill + tip)
    5. Print results

---
layout: quote
---
  
# Starting code:
    
```python
# Step 1: Ask for the bill amount (convert to float)

# Step 2: Ask for the tip percentage (convert to float)

# Step 3: Calculate the tip amount

# Step 4: Calculate the total (bill + tip)

# Step 5: Print results with 2 decimal places

```

---
layout: quote
---
  
# Solution:
    
```python
bill = float(input("What's the bill amount? $"))
tip_percent = float(input("Tip percentage (e.g., 15, 20): "))

tip = bill * (tip_percent / 100)
total = bill + tip

print()
print(f"Bill: ${bill:.2f}")
print(f"Tip ({tip_percent}%): ${tip:.2f}")
print(f"Total: ${total:.2f}")

```


[TRY IT] Try it with a $50 bill and 20% tip.

[MODIFY] Add a line that shows what the tip would be at 15%, 18%, and 20%.