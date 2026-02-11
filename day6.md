# Day 6: Operators
Python has different types of operators for different operations. To create a calculator we require arithmetic operators.
# Arithmetic operators


|   Operator             |Operator Name                          |Example                         |
|----------------|-------------------------------|-----------------------------|
|+|`Addition`            |``` 15+7 ```            |
|-|`Subtraction`            |``` 15-7 ```            |
|*|`Multiplication`            |``` 5*7 ```            |
|**|`Exponential`            |``` 5**3 ```            |
|/|`Division`            |``` 5/3 ```            |
|%|`Modulus`            |``` 15%7 ```            |
|//|`Floor Division`            |``` 15//7 ```            |

- The `%` symbol is the Modulus Operator. It returns the remainder left over after the division is performed.
- The // symbol is the Floor Division Operator. It divides two numbers and "rounds down" the result to the nearest whole integer, effectively chopping off the decimal part.
- 15 // 7:    
  - Perform standard division: 15 / 7 = 2.1428...
  - $Remove the decimal part (floor it).
  - Result: 2
# Exercise
```python
n = 15
m = 7
ans1 = n+m
print("Addition of",n,"and",m,"is", ans1)
ans2 = n-m
print("Subtraction of",n,"and",m,"is", ans2)
ans3 = n*m
print("Multiplication of",n,"and",m,"is", ans3)
ans4 = n/m
print("Division of",n,"and",m,"is", ans4)
ans5 = n%m
print("Modulus of",n,"and",m,"is", ans5)
ans6 = n//m
print("Floor Division of",n,"and",m,"is", ans6)
```
Output:
```markdown
Addition of 15 and 7 is 22
Subtraction of 15 and 7 is 8
Multiplication of 15 and 7 is 105
Division of 15 and 7 is 2.142857142857143
Modulus of 15 and 7 is 1
Floor Division of 15 and 7 is 2
```