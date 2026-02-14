# Day 13: String Methods -3
### 1. Searching Strings: `.find()` vs `.index()`
Both of these methods serve the same primary purpose: To find the index (position) of the first occurrence of a substring.

#### (a) The `.find()` Method:

The `find()` method is "safe." It searches the string and, if it finds the substring, returns the index of the `first character`. If it fails, it returns `-1`.

Example:  
Imagine you are building a search feature. If the user types something that doesn't exist, you don't want the whole website to crash; you just want to know it wasn't found.

```Python
str1 = "He's name is Dan. He is an honest man."

# Python is literal. It ignores "He's" and looks for "is"
print(str1.find("is"))  
# Output: 10 (The 'i' in the first 'is' is at index 10)

# What happens if we look for something that doesn't exist?
print(str1.find("Daniel")) 
# Output: -1
```

#### (b) The `.index()` Method
The `index()` method is "strict." It works exactly like `find()`, but if it fails to find the substring, it raises a ValueError and stops the program.

Example:  
You use `.index()` when your program must find the substring to continue. If it's missing, something is fundamentally wrong with your data, and you want the program to stop (crash) so you can fix it.

```Python
str1 = "He's name is Dan."

# Works just like find when the substring exists
print(str1.index("is")) 
# Output: 10

# CRASHES if it doesn't exist
print(str1.index("Daniel")) 
# Result: ValueError: substring not found
```

### 2. String Validation: `"Is"` Methods
In Python, methods starting with `is` always return a Boolean (True or False). They are used to validate user input, like checking if a password has numbers or if a name has only letters.

#### (a) `.isalnum()` (Alphanumeric):
Checks if the string contains only letters (A-Z, a-z) and numbers (0-9).

Returns False if: There are spaces, symbols ($, #, @), or punctuation (!, .).

```Python
# Real-World Scenario: Validating a Username (No spaces or symbols allowed)
username1 = "Harry123"
username2 = "Harry 123" # Contains a space

print(username1.isalnum()) # Output: True
print(username2.isalnum()) # Output: False (Space is not alphanumeric)
```

#### (b) `.isalpha()` (Alphabetical):
Checks if the string contains only letters (A-Z, a-z).

Returns False if: There are numbers, spaces, or symbols.

Example:  
```Python
# Real-World Scenario: Validating a First Name
first_name = "Harry"
error_name = "Harry00"

print(first_name.isalpha()) # Output: True
print(error_name.isalpha()) # Output: False (Numbers are not alphabetical)
```
#### (c) `.islower()` (Lowercase Check):
Checks if all cased characters in the string are lowercase.

Returns True if: Everything is lowercase.

Returns False if: Even one character is Uppercase.

```Python
# Real-World Scenario: Checking if an email is formatted in lowercase
email = "harry@example.com"
bad_email = "Harry@Example.com"

print(email.islower())     # Output: True
print(bad_email.islower()) # Output: False
```

#### (d) `.isprintable()` (Printable Check):
This checks if the string contains characters that are visible when printed.

Returns False if: The string contains "Non-printable" characters like `\n` (new line) or `\t` (tab).

```Python
text1 = "Hello World"
text2 = "Hello \n World" # Contains a new line character

print(text1.isprintable()) # Output: True
print(text2.isprintable()) # Output: False
```

#### (e) `isspace()` :
The isspace() method returns True only and only if the string contains white spaces, else returns False.
### Example:
```python
str1 = "        "       #using Spacebar
print(str1.isspace())
str2 = "        "       #using Tab
print(str2.isspace())
```
### Output:
```
True
True
 ```

#### (f) `istitle()` : 
The istitile() returns True only if the first letter of each word of the string is capitalized, else it returns False.
### Example:
```python
str1 = "World Health Organization" 
print(str1.istitle())
```
### Output:
```
True
 ```

### Example:
```python
str2 = "To kill a Mocking bird"
print(str2.istitle())
```
### Output:
```
False
 ```

#### (g) `isupper()` :
The isupper() method returns True if all the characters in the string are upper case, else it returns False. 
### Example :
```python
str1 = "WORLD HEALTH ORGANIZATION" 
print(str1.isupper())
```
### Output:
```
True
 ```
  

### (3) `swapcase()` : 
The swapcase() method changes the character casing of the string. Upper case are converted to lower case and lower case to upper case.
### Example:
```python
str1 = "Python is a Interpreted Language" 
print(str1.swapcase())
```
### Output:
```
pYTHON IS A iNTERPRETED lANGUAGE
 ```

### (4) `title()` :
The title() method capitalizes each letter of the word within the string.
### Example:
```python
str1 = "He's name is Dan. Dan is an honest man."
print(str1.title())
```
### Output:
```
He'S Name Is Dan. Dan Is An Honest Man.
```

