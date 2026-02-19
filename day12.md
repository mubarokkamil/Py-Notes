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

Example 1: 
```Python
heading = "Welcome to the Console"
print(len(heading))          # Original length: 22

centered_heading = heading.center(50)
print(centered_heading)

print(len(centered_heading)) # New total length: 50
```
Technical Breakdown:   
If your string is 22 characters long and you call .center(50), Python adds 28 spaces in total (14 on the left, 14 on the right) so the final string length is exactly 50.

Example 2:
```Python
# Dashboard title for a server management tool
title = "SYSTEM STATUS CHECK"

# Centers the title in a 60-character wide terminal
print("=" * 60)
print(title.center(60))
print("=" * 60)
```
```markdown
Output:
============================================================
                    SYSTEM STATUS CHECK                     
============================================================

```
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

### 4. String Validation: The `.endswith()` Method
The `.endswith()` method is used to check if a string finishes with a specific suffix. This is a "Validation Method" that returns a `Boolean value`.

How it Works:
- Input: The string (or substring) you want to look for.
- Output: True if it matches the end exactly, False if it doesn't.

Example:  
Imagine you are building a system where users upload files. You want to make sure they only upload Python files (.py) or Image files (.jpg).

```Python
# Real-world Example: Checking file extensions
filename = "main_script.py"

# Checking if the file is a Python script
is_python_file = filename.endswith(".py")

print(is_python_file)
# Output: True

# Checking for a different extension
is_image = filename.endswith(".jpg")
print(is_image)
# Output: False
```

### 5. String Validation: The `.startswith()` Method
The `.startswith()` method checks if a string begins with a specific sequence of characters. Just like its counterpart, it returns a Boolean (True or False).

How it Works
- Input: The prefix you want to check for.
- Output: True if the string starts with that prefix, False otherwise.

Example:   
Website Protocol Checker:  
When building a web scraper or a link validator, you often need to check if a URL is secure (https) or insecure (http).

```Python
url_1 = "https://www.google.com"
url_2 = "http://unsecure-site.com"

# Checking for secure protocol
print(url_1.startswith("https")) # Output: True
print(url_2.startswith("https")) # Output: False
```

### 6. Advanced Validation: `endswith()` with Start & End Indices
In Python, you don't have to check the very end of a string. You can define a "search area" by providing a start index and an end index.

How the Logic Works
- When you write `str.endswith("suffix", start, end)`:
Python "slices" the string mentally from the start index up to (but not including) the end index.
- It then checks if that specific slice ends with your chosen suffix.

Example:
```python
text = "Welcome to Python"
# Indices:
# W e l c o m e   t o   P  y  t  h  o  n
# 0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15

# Step 1: Slice from index 4 to 10
# result of text[4:10] is "ome to"

# Step 2: Check if "ome to" ends with "to"
result = text.endswith("to", 4, 10)

print(result) 
# Output: True
```


