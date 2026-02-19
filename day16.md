# Day-16: Match Case Statements

Match Case (often called "Structural Pattern Matching") is a more readable way to handle multiple conditions. Instead of writing elif over and over, you "match" a variable against different "patterns."  

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

