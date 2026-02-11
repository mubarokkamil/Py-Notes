# Day 4 - Comments, Escape sequence & Print in Python

# Python Comments
A comment is a part of the coding file that the programmer does not want to execute, rather the programmer uses it to either explain a block of code or to avoid the execution of a specific part of code while testing.

## Single-Line Comments:

To write a comment just add a `#` at the start of the line.

### Example 1

```python
#This is a 'Single-Line Comment'
print("This is a print statement.")
``` 

Output:

```markup
This is a print statement. 
``` 

### Example 2

```python
print("Hello World !!!") #Printing Hello World
```

Output:

```markup
Hello World !!!
``` 

### Example 3:

```python
print("Python Program")
#print("Python Program")
``` 

### Output: 

```markup
Python Program
``` 
## Multi-Line Comments:

While you can use multiple `#` symbols for each line, Python also allows the use of triple quotes (`'''` or `"""`).

**Example 1:** The use of `#`.

```python
#It will execute a block of code if a specified condition is true.
#If the condition is false then it will execute another block of code.
p = 7
if (p > 5):
    print("p is greater than 5.")
else:
    print("p is not greater than 5.")
```


Output:

```markup
p is greater than 5.
```


**Example 2:** The use of multiline string.

```python
'''
This is a multi-line comment
using triple single quotes.
It is very useful for long explanations.
'''

"""
You can also use
triple double quotes
for the exact same purpose.
"""
print("Multi-line comments are great!")
```


### Output

```markup
Multi-line comments are great!
```

## Pro-Tips: IDE Shortcuts
Modern IDEs like VS Code or Replit offer shortcuts to speed up your workflow. Mastering these will make you a much faster programmer:

Bulk Commenting:  
Select one or more lines and press:  
-  `Ctrl` + `/` for Windows/Linux
-  `Command` + `/` for Mac  
to toggle comments on and off.
# Escape Sequence Characters

To insert characters that cannot be directly used in a string, we use an escape sequence character.


An escape sequence character is a backslash  `\`  followed by the character you want to insert.

If you try to press "Enter" inside a `print()` statement, Python will throw an EOL (End of Line) error. Use `\n` instead:
```python
# Using Newline
print("Hey I am a good boy\nand this viewer is also a good boy/girl")

# Using Double Quotes within a string
print("Hey I am a \"good boy\"")
```
### Output

```markup
Hey I am a good boy
and this viewer is also a good boy/girl
Hey I am a "good boy"
```
# More on Print statement
## Multi-Value Printing
You can pass multiple objects into a single print statement by separating them with commas.

```Python
print("Hey", 6, 7)
```
Output:  
```markdown
Hey 6 7
```


## Other Parameters of Print Statement 
1. sep='separator': Specify how to separate the objects, if there is more than one. Default is ' '
2. end='end': Specify what to print at the end. Default is '\n' (line feed)

```python
# Using a custom separator
print("Hey", 6, 7, sep="~") 

# Using a custom end character
print("Hey", 6, 7, end="009\n")
print("Harry")
```

Output:  
```markdown
Hey~6~7
Hey 6 7009
Harry
```
