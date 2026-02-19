# Day-16: Match-Case Statements

Match Case (often called "Structural Pattern Matching") is a more readable way to handle multiple conditions. Instead of writing elif over and over, you "match" a variable against different "patterns."  

Unlike languages like C++ or Java, Python’s match case does not require a break statement. Once it finds a match, it runs that block and automatically stops. No "falling through" to the next case!
## General Syntax:
```Python
match variable_name:
    case pattern1:
        # Executes if variable strictly matches pattern1
        
    case pattern2 if condition:
        # Only executes if variable == pattern2 & the extra 'if condition' is also True.
        
    case pattern3:
        # Executes if variable matches pattern3
        
    case _:
        # Executes if none of the above matched.
```

Example:
```python
status = 404

match status:
    case 200:
        print("Success")
    case 400:
        print("Bad Request")
    case 404:
        print("Not Found")
    case 500 | 501:  # You can use | (or) to group patterns
        print("Server Error")
    case _:
        print("Unknown Status")
```
Output:
```
Not Found
```

Example:

The student's score
```python
score = int(input("Enter your marks: "))

match score:
    case n if n >= 80:
        print("Grade: A+ | You're a legend!")
        
    case n if n >= 75:
        print("Grade: A | Solid work, keep it up!")
        
    case n if n >= 70:
        print("Grade: A- | Good progress.")
        
    case n if n >= 60:
        print("Grade: B | You passed!")
        
    case n if n >= 50:
        print("Grade: C | You passed!")
    case n if n >= 40:
        print("Grade: D | You passed!")
        
    case _:
        print("Grade: F")
```

