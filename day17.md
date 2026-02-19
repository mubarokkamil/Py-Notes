# Day-17: The "For Loop" & Range

A for loop is used to "iterate" over a sequence.

General Syntax:
```Python
for variable in iterable:
    # Code to execute for each item
```

### Example:  iterating over a string:  
In Python, a string is an iterable.
That means Python can go through it character by character.
```python
name = 'Abhishek'
for i in name:
    print(i)
```

Output:
```
A
b
h
i
s
h
e
k
```
### Step-by-Step Explanation: How the Loop Works

When you run `for i in name:`, Python doesn't just see a word; it sees a sequence of positions. It starts at the very beginning (Index 0) and moves through to the end.


Here is what happens in the computer's memory during each "lap" of the loop:

| Iteration | Current Index | Variable `i` becomes... | Output |
| :--- | :--- | :--- | :--- |
| 1st | `0` | `'A'` | `A` |
| 2nd | `1` | `'b'` | `b` |
| 3rd | `2` | `'h'` | `h` |
| 4th | `3` | `'i'` | `i` |
| 5th | `4` | `'s'` | `s` |
| 6th | `5` | `'h'` | `h` |
| 7th | `6` | `'e'` | `e` |
| 8th | `7` | `'k'` | `k` |



---

### The Logic Breakdown:
1. **The Starting Point:** Python looks at the character at **Index 0**. It assigns that character to your variable `i`.
2. **The Action:** It executes the code inside (in this case, `print(i)`).
3. **The Increment:** Python automatically moves to **Index 1**, updates `i` to the new character, and repeats.
4. **The Termination:** Once Python reaches the end of the string and sees there is no "Index 8," it gracefully exits the loop.


### Example: iterating over a list:

```python
fruits = ["🍎 Apple", "🍌 Banana", "🍒 Cherry"]

for x in fruits:
    print(x)
```
Output:
```
🍎 Apple
🍌 Banana
🍒 Cherry
```


### Example:

```python
scores = [45, 88, 72, 91, 58]

for score in scores:
    if score >= 60:
        print(f"Score {score}: Passed! ✅")
    else:
        print(f"Score {score}: Failed. ❌")
```

Output:
```
Score 45: Failed. ❌
Score 88: Passed! ✅
Score 72: Passed! ✅
Score 91: Passed! ✅
Score 58: Failed. ❌
```

## The `range()` Function:
The `range()` function generates a sequence of numbers. It is the most common way to run a loop a specific number of times.

### Syntax Variations: 
- **`range(stop)`:** Starts at 0, ends at `stop - 1`.

- **`range(start, stop)`:** Starts at start, ends at `stop - `1`.

- **`range(start, stop, step)`:** Starts at start, ends at `stop - 1`, and skips numbers by the step value.

- `range(1, 5)` is math notation for `[1, 5)`, meaning $1 \leq x < 5$.

### `range(1, 12, 3)`:  
- starts at 1.
- It adds 3: 1 + 3 = 4.
- It adds 3: 4 + 3 = 7.
- It adds 3: 7 + 3 = 10.
- Next would be 13, but that's past our limit (12), so it stops!


#### Example:
```python
for k in range(5):
    print(k)
```
Output:  
```
0
1
2
3
4
```

Example:
```python
for k in range(2,6):
    print(k)
```
Output:  
```
2
3
4
5
```

Example:
```python
for i in range(2,16,3):
    print(i)
```

Output:  
```
2
5
8
11
14
```

## Counting Backwards: 
To count down, your start must be higher than your stop, and you must use a negative step.

Example:
```Python
for i in range(5, 0, -1):
    print(i)
```
Output:  
```
5
4
3
2
1
```
Example:

```python
for i in range(5, 0, -2):
    print(i)
```
Output:  
```
5
3
1
```

## Nested `for` Loops (Loop inside a Loop):
You can put a loop inside another loop. This is useful for complex data, like a list of words where you want to inspect every letter of every word.  
The inner loop must finish all its iterations before the outer loop can move forward by just one step.

Example:
```Python
colors = ["Red", "Green"]

for color in colors:
    print(f"Current Color: {color}")
    for letter in color:
        print(f"  Character: {letter}")
```

Output:
```
Current Color: Red
  Character: R
  Character: e
  Character: d
Current Color: Green
  Character: G
  Character: r
  Character: e
  Character: e
  Character: n
```


### Example: The "Pixel Grid" (Image Processing Theory)   
Digital images are just grids of pixels. To change the brightness of an image, a computer uses a nested loop to visit every Row and every Column (X and Y coordinates).  
```python
# A 3x3 image grid (simplified)
rows = 3
columns = 3

for y in range(rows):         # Outer Loop: Vertical position
    for x in range(columns):  # Inner Loop: Horizontal position
        print(f"[{x},{y}]", end=" ") # end=" " keeps it on one line
    print() # New line after each row is done
```
Output:
```
[0,0] [1,0] [2,0] 
[0,1] [1,1] [2,1] 
[0,2] [1,2] [2,2]
```

## Project-1: The "Digital Concert Ticket" Generator:

You are organizing a small underground concert. There are 3 Rows, and each row has 5 Seats. You need to print a ticket for every single seat in the house.

```Python
rows = ["Row A", "Row B", "Row C"]
seats = range(1, 6) # Seats 1, 2, 3, 4, 5

for r in rows:         
    for s in seats:     
        print(f"Ticket Issued: {r} - Seat {s}")
    print("-" * 20)
```

Output:
```
Ticket Issued: Row A - Seat 1
Ticket Issued: Row A - Seat 2
Ticket Issued: Row A - Seat 3
Ticket Issued: Row A - Seat 4
Ticket Issued: Row A - Seat 5
--------------------
Ticket Issued: Row B - Seat 1
Ticket Issued: Row B - Seat 2
Ticket Issued: Row B - Seat 3
Ticket Issued: Row B - Seat 4
Ticket Issued: Row B - Seat 5
--------------------
Ticket Issued: Row C - Seat 1
Ticket Issued: Row C - Seat 2
Ticket Issued: Row C - Seat 3
Ticket Issued: Row C - Seat 4
Ticket Issued: Row C - Seat 5
--------------------
```

## Project-2: The "School Timetable" Builder:
You want to map out your study schedule. You have 3 Study Days, and on each day, you have 2 Subjects to cover (Math and Coding).

```Python
days = ["Monday", "Tuesday", "Wednesday"]
subjects = ["Python Math", "Python Logic"]

for day in days:
    print(f"📅 Schedule for {day}:")
    
    for sub in subjects:
        print(f"  📖 Study: {sub}")
        
        for session in range(1, 3):
            print(f"    ⏱️ Session {session} complete.")

    print("✅ Day complete!\n")
```

Output:
```
📅 Schedule for Monday:
  📖 Study: Python Math
    ⏱️ Session 1 complete.
    ⏱️ Session 2 complete.
  📖 Study: Python Logic
    ⏱️ Session 1 complete.
    ⏱️ Session 2 complete.
✅ Day complete!

📅 Schedule for Tuesday:
  📖 Study: Python Math
    ⏱️ Session 1 complete.
    ⏱️ Session 2 complete.
  📖 Study: Python Logic
    ⏱️ Session 1 complete.
    ⏱️ Session 2 complete.
✅ Day complete!

📅 Schedule for Wednesday:
  📖 Study: Python Math
    ⏱️ Session 1 complete.
    ⏱️ Session 2 complete.
  📖 Study: Python Logic
    ⏱️ Session 1 complete.
    ⏱️ Session 2 complete.
✅ Day complete!
```

