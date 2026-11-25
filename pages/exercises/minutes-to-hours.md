---
layout: quote
---


# Exercise: Minutes to Hours

Asks for total minutes and converts it into hour and minutes, so 90 minutes → 1 hour and 30 minutes

<div v-click>
  <iframe
    v-if="$clicks >= 1"
    src="https://trinket.strivemath.org/embed/python3/c1135f0b8de7?outputOnly=true&runOption=run&start=result"
    class="w-full h-80 rounded-lg border border-gray-500/40 mt-6"
  ></iframe>
</div>


---
layout: quote
---

    
# Instructions
1. take input for total minutes
2. convert it into hours and get leftover minutes
3. print hours and leftover minutes

---
layout: quote
---


# Starting Code
    
```python
# Step 1: take input

# Step 2: convert into hours and get leftover minutes

# Step 3: print the hours and leftover minutes
```

---
layout: quote
---

# Solution
    
```python
# Step 1: take input
total = int(input("Type number of minutes: "))
print()

# Step 2: convert into hours and get leftover minutes
hours = total // 60
minutes = total % 60

# Step 3: print the hours and minutes
print(f"That's {hours} hours and {minutes} minutes.")
```