# Code Tracing Answer Key ✅

> Note: Short explanatory notes about **functions (parameters as placeholder variables), counting from 0 (indexing), and slicing/range rules** are included at the bottom of this file.

This file gives the expected console outputs for the three worksheets in order: **CT1**, **CT2**, **CTASC**. Each question is numbered 1–15 in its section.

---

## CT1 — `codeTracing1.py` (Q1–Q15)

1.
```
16
```
Note: operator precedence — `*` before `+`.

2.
```
3
2
```
Note: first `//` (integer division), then `%` (remainder).

3.
```
21
```

4.
```
11
```
Note: `len('Python Game')` counts the space.

5.
```
Total is: 15
```
Note: `int('10')` converts the string to an integer before adding.

6.
```
Incorrect
```

7.
```
Player: Zoe
Score: 95
```

8.
```
2
4
6
```
Note: `range(1,4)` yields 1,2,3 — loop variable starts at the `start` value given.

9.
```
17
```
Note: result of `(a * 2) - b` with `a=10, b=3`.

10.
```
Outside activity
```
Note: `elif temp > 10 or is_sunny` is true here.

11.
```
3
```
Note: counts even `i` values in `range(5)` → 0,2,4.

12.
```
1
2
4
5
```
Note: `continue` skips printing when `count == 3`.

13.
```
Minor
```

14.
```
B6
```
Note: `item1` is `'B'`; after `.append('F')` the length is 6.

15.
```
10
```
Note: first `if` branch runs (not game_over and score == 0).

---

## CT2 — `codeTracing2-harder.py` (Q1–Q15)

1.
```
20
50
80
```
Note: `range(2,10,3)` → 2,5,8; printed values multiplied by 10.

2.
```
12
9
6
```
Note: `while j > 5` with `j -= 3` stops once j <= 5.

3.
```
4
```

4.
```
6
```
Note: `break` stops loop when `num == 4` — sum is 1+2+3.

5.
```
hlo
```
Note: indexes used are 0,2,4 (even indices) from `'hello'`.

6.
```
3
```
Note: `data[1:4]` contains 3 items (indices 1,2,3).

7.
```
['green', 'blue', 'yellow']
```
Note: `colors[1:-1]` slices from index 1 up to (not including) the last.

8.
```
[20, 25, 5, 10]
```
Note: concatenation `scores[3:] + scores[:2]` preserves order.

9.
```
['A', 'C', 'E', 'G']
```
Note: `letters[::2]` uses a step of 2 → every other element.

10.
```
['c', 'b', 'a']
```
Note: `items[::-1]` reverses the list (step -1).

11.
```
[3, 5, 7, 9]
```
Note: in-place update `numbers[i] = numbers[i] * 2 + 1`.

12.
```
HEL
```
Note: `pop(0)` removes the first item three times and builds the string.

13.
```
[4, 9, 16]
```

14.
```
3
```
Note: `players[1:4]` yields three names (indices 1,2,3).

15.
```
[30, 40]
```
Note: commands remove first inventory items twice, leaving [30,40].

---

## CTASC — `codeTracing3-ASCII-art.py` (Q1–Q15)

1.
```
****
****
****
```

2.
```
#
##
###
```

3.
```
***
 **
  *
```
Note: inner `col < row` produces leading spaces on lower rows.

4.
```
XOXO
OXOX
XOXO
OXOX
```

5.
```
+++++
+   +
+   +
+++++
```
Note: border condition uses `row == 0 or row == 3 or col == 0 or col == 4`.

6.
```
   *
  **
 ***
****
```

7.
```
1 2 3
2 4 6
3 6 9
```

8.
```
/    
 /   
  /  
   / 
    /
```
Note: diagonal printed when `row == col`.

9.
```
  *  
 *** 
*****
 *** 
  *  
```

10.
```
| | | 
| | | 
| | | 
| | | 
| | | 
```

11.
```
   *   
  ***  
 ***** 
*******
```

12.
```
X^^^
VX^^
VVX^
```

13.
```
#######
#     #
#  O  #
#     #
#######
```

14.
```
=====
-----
=====
-----
```

15.
```
       
   *   
  *O*  
 *OXO* 
  *O*  
   *   
       
```
Note: concentric pattern using Manhattan distance from center (3,3).

---

## Concept notes — functions, indexing, slicing, and `range()`

- **Function definition vs call (teacher ↔ student analogy):**
  - Definition: teacher writes the lesson plan (`def greet(name):`) — it **defines** what will happen but does not run it.
  - Call: teacher *calls on a student* to perform the lesson (`greet('Sasha')`) — this **runs** the function.

- **Parameters vs arguments (placeholder variables):**
  - **Parameters** are the names in the function definition — they are *placeholder variables* (named slots the function uses), e.g., `def add(a, b):` → `a`, `b` are parameters.
  - **Arguments** are the actual values passed in when calling the function, e.g., `add(2, 3)` → `2`, `3` are arguments.

- **Indexing & `range()` (counting rules):**
  - Python sequences are **zero-indexed**: the first element is index `0`.
  - `range(n)` → produces `0, 1, ..., n-1`. `range(start, stop)` begins at `start` and stops *before* `stop` (stop is exclusive).
    - e.g. `range(5)` → `0..4`; `range(1,5)` → `1..4` (different starting value).

- **Slicing `[start:stop:step]` (inclusive/exclusive):**
  - `start` is included, `stop` is excluded: `lst[1:4]` returns indices `1,2,3`.
  - Omitting `start` or `stop` uses sequence ends (`[:n]`, `[n:]`). Negative indices count from the end (`-1` is last item).

