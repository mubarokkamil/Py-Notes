# Day 12: String Methods -2

### 1. The `.capitalize()` Method:
The `capitalize()` method is unique because it doesn't just uppercase the first letter; it also standardizes the rest of the string.

How it works:
- Converts the first character to uppercase.
- Converts all other characters to lowercase.
- If the first character is already a capital letter, it remains unchanged, but the rest of the string is still forced to lowercase.

Example:
```Python
# Realistic Blog Heading Example
blog_title = "introduction tO jS"

# Applying capitalize
formatted_title = blog_title.capitalize()

print(formatted_title)
# Output: "Introduction to js"
```
Note: Notice how it fixed the accidental "tO" and "jS"? It’s a "cleaning" method that ensures your titles look professional regardless of human typing errors.

### 2. The `.center()` Method:
The `center()` method aligns your string to the center of a specified width by padding it with characters (usually spaces) on both sides.

How it works:
- It takes an integer argument (the total width you want the string to occupy).
- It calculates the padding needed to put the text in the middle.

Example: 
```Python
heading = "Welcome to the Console"
print(len(heading))          # Original length: 22

centered_heading = heading.center(50)
print(centered_heading)

print(len(centered_heading)) # New total length: 50
```
Technical Breakdown:   
If your string is 22 characters long and you call .center(50), Python adds 28 spaces in total (14 on the left, 14 on the right) so the final string length is exactly 50.


### 3. The `.count()` Method:
The `count()` method is used for basic data analysis. It returns the number of times a specific value appears in the string.

How it works:
- It searches for the exact substring you provide.
- It is case-sensitive (e.g., "Harry" is different from "harry").

Example:
```Python
data = "Harry is a good teacher, Harry loves to code."

# Counting occurrences of "Harry"
occurence_count = data.count("Harry")

print(occurence_count)
# Output: 2.
```

