# Day-14: If-Else-Conditionals

## Comparison Operators:
| Operator | Meaning | Example (age = 20) | Result |
| :--- | :--- | :--- | :--- |
| `>` | Greater than | `age > 18` | `True` |
| `<` | Less than | `age < 18` | `False` |
| `>=` | Greater than or equal to | `age >= 18` | `True` |
| `<=` | Less than or equal to | `age <= 18` | `False` |
| `==` | Equal to (Double equals!) | `age == 18` | `False` |
| `!=` | Not equal to | `age != 18` | `True` |


## if-else Statements:
Sometimes the programmer needs to check the evaluation of certain expression(s), whether the expression(s) evaluate to True or False. If the expression evaluates to False, then the program execution follows a different path than it would have if the expression had evaluated to True.

Based on this, the conditional statements are further classified into following types:
- if
- if-else
- if-elif-else
- nested if-else-elif.


## 1. Simple if Statement:
Use this when you only care if a condition is met, and if it's not, you just want the program to keep running normally.  
Syntax:  

```Python
if condition:
    # Code to execute if condition is True
```
Example:  
```Python
speed = 90
if speed > 80:
    print("🚨 Slow down! You're breaking the limit.")
```
Output:
```
🚨 Slow down! You're breaking the limit.
```

## 2. if-else Statement:
This is your classic "Either/Or" scenario. If the first condition fails, the else block must run.

Syntax:

```Python
if condition:
    # Code to execute if condition is True
else:
    # Code to execute if condition is False
```

Example:
```python
age = 17
if age >= 18:
    print("✅ Welcome to the club!")
else:
    print("❌ Sorry, go home and drink some juice.")
```
Output:
```
❌ Sorry, go home and drink some juice.
```


## 3. if-elif-else Statement:
`elif` is short for `Else If`. Use this when you have multiple specific conditions to check. Python checks them from top to bottom and stops at the first True one.

Syntax:

```Python
if condition1:
    # Code if condition1 is True
elif condition2:
    # Code if condition2 is True
else:
    # Code if none of the above are True
```

Example: "The Grade Calculator"

```Python
score = 85

if score >= 90:
    print("🏆 Grade: A+")
elif score >= 80:
    print("🥈 Grade: B")
elif score >= 70:
    print("🥉 Grade: C")
else:
    print("📚 Keep studying, you can do it!")
```

Output: 
```
🥈 Grade: B
```

