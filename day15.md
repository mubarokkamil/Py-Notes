# Day-15: Nested if-else-elif

This is a decision inside another decision. It’s used for "Layered Logic"

Syntax:

```Python
if condition1:
    if internal_condition:
        # Code if both are True
    else:
        # Code if only condition1 is True
else:
    # Code if condition1 is False
```

Example 1:  

```python
homework_done = True
grade = "B"

# Main Level: The "Gatekeeper" condition
if homework_done == True:
    print("Mom: Since your homework is done, you can go out!")
    
    # --- START OF NESTED LAYER ---
    if grade == "A":
        print("Dad: And since you got an A, here is $50! Have fun.")
    elif grade == "B":
        print("Dad: Good job on the B. Here is $20 for snacks.")
    else:
        print("Dad: You can go, but no extra pocket money this time.")
    # --- END OF NESTED LAYER ---

else:
    print("Mom: No way! Finish your math homework first.")
```
Output:
```
Mom: Since your homework is done, you can go out!
Dad: Good job on the B. Here is $20 for snacks.
```

Example 2:
```python
card_inserted = True
pin_correct = False

if card_inserted == True:
    print("Card detected...")
    if pin_correct == True:
        print("Access Granted. How much cash do you want?")
    else:
        print("Wrong PIN. Card Blocked for security!") # Nested Else
else:
    print("Please insert your card first.")
```
Output:
```
Card detected...
Wrong PIN. Card Blocked for security!
```

