# Day 10: String Slicing and Length

## 1. Finding the Length of a String

Before slicing, you often need to know how many characters are in a string. Python provides the `len()` function for this.

```python
name = "Harry, Shubh"
print(len(name)) # Output: 12 (including the comma and space)

fruit = "Mango"
mango_len = len(fruit)
print(mango_len) # Output: 5
```

## 2. String Slicing Basics
In Python, a string is like an array of characters. You can access parts of it using Square Brackets `[]`.

Key Rules:
- Zero-based Indexing: Counting starts at 0, not 1.
- The Slicing Syntax: `string[start : end]`
- Inclusion Rule: It includes the start index but excludes the end index (it goes up to `end - 1`).

Example:
```Python
fruit = "Mango"

# Accessing characters 0, 1, 2, and 3 (Excludes 4)
print(fruit[0:4]) # Output: Mang

# Accessing characters 1, 2, and 3
print(fruit[1:4]) # Output: ang
```

Shortcuts
- Skip the Start: `fruit[:4]` is the same as `fruit[0:4]`. 

- Skip the End: `fruit[1:]` is the same as `fruit[1:5]`. Python assumes the total length of the string.


## 3. Negative Slicing
Negative slicing allows you to count backwards from the end of the string.

How to Decode Negative Slicing:  
- When Python sees a negative index, it internally adds the length of the string to that number.

Formula:  
 `fruit[-a : -b]` is equivalent to `fruit[len(fruit)-a : len(fruit)-b]`

Example:
```Python
fruit = "Mango" # Length is 5
print(fruit[0:-3]) 

# Calculation:
# fruit[0 : 5-3] 
# fruit[0 : 2]
# Output: Ma
```

Example:

```python
nm = "Zosna Begum"
print(nm[-4:-2])
```
Output:
```markdown
eg
```
Simple Explanation:
- Length of "Zosna Begum" is 11.
- `nm[-4:-2]` is processed as `nm[11-4:11-2]`= `nm[7:9]`.
- We take characters from index 7 up to 8 (but not including 9).

Example:
```python
nm = "Zosna Begum"
print(nm[-4:])
```
Output: 
```markdown
egum  
```
Explanation:  
- `nm[-4:]` is processed as `nm[11-4:11]` = `nm[7:11]`


Example:
```python
nm = "Zosna Begum"

# 1. [:] -> Copy of the whole string
# It starts from the beginning and goes to the very end.
print(nm[:])          # Output: Zosna Begum

# 2. [start:] -> From 'start' index to the very end
# Here we start at index 6 (the letter 'B').
print(nm[6:])         # Output: Begum

# 3. [:stop] -> From the beginning up to 'stop - 1'
# It starts at 0 and stops before index 5 (the space).
print(nm[:5])         # Output: Zosna

# 4. [::2] -> Every 2nd character (skipping 1)
# It takes index 0, skips 1, takes 2, skips 3, and so on.
print(nm[::2])        # Output: ZsaBgm

# 5. [::3] -> Every 3rd character (skipping 2)
# It takes index 0, skips 1,2 takes 3, skips 4,5 and so on.
print(nm[::3])        # Output: ZnBu

# 5. [::-1] -> Reverses the string
# The negative step (-1) tells Python to read the string backwards.
print(nm[::-1])       # Output: mugeB ansoZ
```