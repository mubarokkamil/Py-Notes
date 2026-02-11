# Day 11: String Methods

## 1. The Core Concept: Immutability
In Python, Strings are immutable. This means once a string object is created in memory, its value cannot be changed.

## 2. String Manipulation

### (a) Changing Case: `.upper()` and `.lower()`
These methods are essential for "normalizing" data (e.g., making sure "User1" and "user1" are treated the same).

```Python
blog_title = "Python Programming"

# Converts everything to uppercase
print(blog_title.upper()) # Output: PYTHON PROGRAMMING

# Converts everything to lowercase
print(blog_title.lower()) # Output: python programming

# PROOF OF IMMUTABILITY:
print(blog_title) 
# Output: Python Programming (The original variable remains unchanged!)
```

### (b) Cleaning Data:  `.rstrip()` and `.strip()`

The `strip()` method removes any `white spaces` before and after the string.

Example:
```python
str2 = "   Silver Spoon   "
print(str2.strip())
# Output:Silver Spoon
# Remove 'white space' before and after 'Silver Spoon'
```

The `rstrip()` (Right Strip) method is used to remove specific characters from the end of a string. This is commonly used to clean up trailing punctuation or whitespace.

```Python
raw_data = "Harry!!!!!!!"

# Removes the '!' only from the right side
clean_data = raw_data.rstrip("!")

print(clean_data) 
# Output: Harry

# IMPORTANT: It does NOT remove leading characters
leading_data = "!!!Harry!!!"
print(leading_data.rstrip("!")) 
# Output: !!!Harry
```

### (c) Search and Replace: `.replace()`
This method searches for a specific substring and replaces it with another. It is case-sensitive and replaces all occurrences by default.

```Python
sentence = "Harry is a coder. Harry is learning Python."

# Syntax: string.replace(old_value, new_value)
new_sentence = sentence.replace("Harry", "John")

print(new_sentence)
# Output: John is a coder. John is learning Python.
```

## (d) The `.split()` Method:
The `.split()` method breaks a single string into multiple parts based on a separator (delimiter). It packages these parts into a List.
- Syntax: `.split("separator")`
- Input: A single String.
- Output: A List containing substrings.

The `.split()` method takes an optional argument called a separator. If you don't provide one, it defaults to any `whitespace`. However, you can pass any character (or string) inside the parentheses.

Example:  
#### 1. Splitting by space:
```Python
blog_post = "Introduction to Python Strings"

# Splitting by space " "
words = blog_post.split(" ")

print(words)
# Output: ['Introduction', 'to', 'Python', 'Strings']
```
N.B: `words = blog_post.split(" ")` is same as `words = blog_post.split()`.  

#### 2. The CSV Style (Comma Separated):
This is how programs read data from spreadsheets (CSV stands for Comma Separated Values).

```Python
# A string representing a user record
user_data = "John,Doe,25,New York"

# We split at every comma
fields = user_data.split(",")

print(fields)
# Output: ['John', 'Doe', '25', 'New York']
```


#### 3. The URL/Path Style (Slash Separated):
When working with web addresses or file paths, you often need to break down the folders or segments.

```Python
url = "https://github.com/user/repository"

# We split at the forward slash "/"
segments = url.split("/")

print(segments)
# Output: ['https:', '', 'github.com', 'user', 'repository']
```
Note: Notice the empty string `''` in the list. This happens because there are two slashes together `(//)`, and Python finds "nothing" between them.

#### 4. The Date/ID Style (Hyphen Separated):
Common for processing dates or product serial numbers.

```Python
date_string = "2026-02-10"

# Splitting by hyphen "-"
date_parts = date_string.split("-")

print(date_parts)

# Output:['2026', '02', '10']
```

#### 5. Multicharacter Separators:
You aren't limited to just one character. You can split by a whole word or a sequence.

```Python
text = "Apple and Orange and Banana"

# Splitting by the word " and "
fruits = text.split(" and ")

print(fruits)
# Output: ['Apple', 'Orange', 'Banana']
```

