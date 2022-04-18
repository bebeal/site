---
weight: 21
title: Coding Questions
---

# Practice Problems

---

There are much cleaner solutions to many of these problems, I am showing verbose solutions in an attempt to provide more clarity.


You may **NOT** use the following list methods: reverse(), sort(), copy(), count()

You may **NOT** use the following string methods: zfill(), swapcase(), replace(), join(), count()

You may **NOT** use the following built-in functions: sum(), sorted(), reversed()

## Basic

### get_gpa

Complete a function named get_gpa that calculates and returns a student's GPA given the number of A's, B's, C's, D's, and F's the student has earned in classes.

Recall GPA is equal to (grade points earned) / (total credit hours attempted)

The number of each letter grade earned (A, B, C, D,  and F) are sent as parameters to the method. Assume every class the student takes is worth 3 credits. A's are worth 4 grade points per credit, B's are worth 3 grade points per credit, C's are worth 2 grade points per credit, D's are worth 1 grade point per credit, and F's are worth 0 grade points.

For example, given a student with 3 A's, 4 B's, 1 C, 0 D's, and 2 F's the method returns a GPA of 2.6.

For this question you must write the function definition including parameters and the return statement.

{{< details title="Show Solution" open=false >}}

```python
def get_gpa(a, b, c, d, f):
    return ((a * 4 + b * 3 + c * 2 + d)
            / (a + b + c + d + f))
```
{{< /details >}}
<sup>source: Summer 2020 Midterm</sup>


<br>

## Conditionals

### print_wind_classificication

Complete the following function. Do not repeat the function header in your answer. Just complete the code of the function.

```python
# print the wind speed classification based
# on the given wind speed in miles per hour.
def print_wind_classification(speed):
```

The parameter speed stores an integer and it represents the current wind speed in miles per hour. Assume speed stores a value >= 0.

The function prints the classification of the given wind speed based on the following criteria: Note the [ symbol means inclusive and the ) symbol means exclusive.

```
[0, 3) -> Calm
[3, 10) -> Light
[10, 20) -> Moderate
[20, 45) -> Strong
>= 45 -> Violent
```

So for example if speed stored the value 20 the function would print out Strong and nothing else.

{{< details title="Show Solution" open=false >}}

```python
# print the wind speed classification based
# on the given wind speed in miles per hour.
def print_wind_classification(speed):
    if speed < 3:
        print('Calm')
    elif speed < 10:
        print('Light')
    elif speed < 20:
        print('Moderate')
    elif speed < 45:
        print('Strong')
    else:
        print('Violent')
```
{{< /details >}}
<sup>source: Summer 2020 Midterm</sup>


<br>

## Loops

### rolls_to_get_total

Complete the following function. Do not repeat the function header in your answer. Just complete the code of the function.

```python
# roll a die until the sum of the rolls is >= goal.
# Return the number of rolls it took to reach the goal.
def rolls_to_get_total(sides, goal):
```

The parameter named sides represents the number of sides on a die, a single dice. Goal represents the total we are trying to reach. Assume sides and goal are both integers and both store values greater than 0.

The method performs a simulation, rolling a die with the given number of sides and adding up the results until the sum of the rolls is greater than or equal to goal. The method then returns the number of rolls of the die it took to reach the goal.

You may assume the randint function from the random module has already been imported. Recall, randint(1, 6) would return a random integer from 1 to 6 inclusive with each value being equally likely.

{{< details title="Show Solution" open=false >}}

```python
# roll a die until the sum of the rolls is >= goal.
# Return the number of rolls it took to reach the goal.
def rolls_to_get_total(sides, goal):
    total = 0
    count = 0
    while total < goal:
        total += randint(1, sides)
        count += 1
    return count
```
{{< /details >}}
<sup>source: Summer 2020 Midterm</sup>


<br>

### print_areas

Complete the following function. Do not repeat the function header in your answer. Just complete the code of the function.

```python
# print out the areas of all squares with integer widths between
# [1, max_width] and integer heights between [1, max_height].
def print_areas(max_width, max_height):
```

The parameters max_width and max_height shall store integer values >= 1. The function prints out all areas of the squares as the width, and height of the square, vary from 1 to the given maximum value.

For example if max_width stored 2 and max_height stored 4 the function would print out the following:

```
width = 1 height = 1 area = 1
width = 1 height = 2 area = 2
width = 1 height = 3 area = 3
width = 1 height = 4 area = 4
width = 2 height = 1 area = 2
width = 2 height = 2 area = 4
width = 2 height = 3 area = 6
width = 2 height = 4 area = 8
```

Use nested for loops and the range function in your answer.

{{< details title="Show Solution" open=false >}}

```python
# print out the areas of all squares with integer widths between
# [1, max_width] and integer heights between [1, max_height].
def print_areas(max_width, max_height):
    for width in range(1, max_width + 1):
        for height in range(1, max_height + 1):
            area = width * height
            print('width =', width, 'height =', height, 'area =', area)
```
{{< /details >}}
<sup>source: Summer 2020 Midterm</sup>


<br>


### get_fibonacci

Complete the following function. Do not repeat the function header in your answer. Just complete the code of the function.

```python
# Return the nth Fibonnaci number. We use 1 based indexing.
# f(1) = 1, f(2) = 1, f(3) = 2, ...
def get_fibonacci(n):
```

The function returns the nth Fibonnaci number. Assume n stores an integer >= 1.

We define the first and second Fibonnaci numbers to equal 1. The nth Fibonnaci number, for n >= 3, is the sum of the previous 2 Fibonacci numbers. fib(n) = fib(n - 2)+ fib(n - 1)

Examples:

```
get_fibonacci(1) -> returns 1
get_fibonacci(2) -> returns 1
get_fibonacci(3) -> returns 2 (1 + 1)
get_fibonacci(4) -> returns 3 (1 + 2)
get_fibonacci(5) -> returns 5 (2 + 3)
get_fibonacci(6) -> returns 8 (3 + 5)
...
get_fibonacci(12) -> returns 144 (55 + 89)
```

{{< details title="Show Solution" open=false >}}

```python
# Return the nth Fibonnaci number. We use 1 based indexing.
# f(1) = 1, f(2) = 1, f(3) = 2, ...
def get_fibonacci(n):
    two_back = 1
    one_back = 1
    for i in range(3, n + 1):
        two_back, one_back = one_back, two_back + one_back
    return one_back
```
{{< /details >}}
<sup>source: Summer 2020 Midterm</sup>


<br>

## Strings

### second_half_letters

Write a function `second_half_letters`, that accepts a string as its parameter and returns an integer representing how many of of the letters in the string come from the second half of the alphabet. Compare case-insensitively, such that uppercase values of 'N' through 'Z' count, as well as lowercase values of 'n' through 'z' count.

```
second_half_letters('Nasir Ahmed') ⟶ returns 3 
second_half_letters('David Huffman') ⟶ returns 3 
second_half_letters('Claude Shannon') ⟶ returns 6
```

```python
def second_half_letters(phrase):
    # Complete the function
```
{{< details title="Show Solution" open=false >}}

```python
def second_half_letters(phrase):
    count = 0
    # Convert to lower case so we only check [n, z]
    phrase = phrase.lower()
    for char in phrase:
        if 'n' <= char <= 'z':
            count += 1
    return count
```
{{< /details >}}
<sup><a href='https://practiceit.cs.washington.edu/problem/view/bjp3/chapter4/s24-secondHalfLetters'>source</a></sup>


<br>

### replace

Write a function called `replace` that accepts a source string, a target string, and a replacement string. The function returns a new string with all occurrences of the target string in the source string replaced with the given replacement string. Characters in the source string that are not equal to the target character appear unchanged in the resulting string and in the same relative order they appeared in the source string. 

```
replace('Larry', 'r', 'great') ⟶ returns 'Lagreatgreaty' 
replace('Tim', 't', 'J') ⟶ returns 'Tim' 
replace('CS303E', '0', '1') ⟶ returns 'CS313E'
```

```python
def replace(source, target, replacement):
    # Complete the function
```
{{< details title="Show Solution" open=false >}}

```python
def replace(source, target, replacement):
    result = ''
    for ch in source:
        if ch == target:
            result += replacement
        else:
            result += ch
    return result
```
{{< /details >}}
<sup><a href='https://www.cs.utexas.edu/~scottm/cs312/handouts/tests/FA_19_E1.pdf'>source</a></sup>


<br>

## Lists

### count_factors

Write a function `count_factors`, that accepts an integer (positive) as its parameter and returns a list of its positive factors. Example: The 6 factors of 12 are 1, 2, 3, 4, 6, and 12.

```
count_factors(12) ⟶ returns [1, 2, 3, 4, 6, 12]
count_factors(15) ⟶ returns [1, 3, 5, 15]
count_factors(17) ⟶ returns [1, 17]
```


```python
def count_factors(num):
    # Complete the function
```
{{< details title="Show Solution" open=false >}}

```python
def count_factors(num):
    factors = []
    for i in range(1, num + 1):
        if num % i == 0:
            factors.append(i)
    return factors
```

{{< /details >}}
<sup><a href='https://practiceit.cs.washington.edu/problem/view/bjp5/chapter4/s16-countFactors'>source</a></sup>


<br>

### percent_even

Write a function called `percent_even` that accepts a list of integers as a parameter and returns the percentage of even numbers in the array as a real number. For example, if the list stores the elements [6, 2, 9, 11, 3], then your function should return 40.0.

```
percent_even([6, 2, 9, 11, 3]) ⟶ returns 40.0 
percent_even([2]) ⟶ returns 100.0 
percent_even([11, 19, 5, 97]) ⟶ returns 0.0
```

```python
def percent_even(data):
    # Complete the function
```
{{< details title="Show Solution" open=false >}}

```python
def percent_even(data):
    count = 0
    for i in range(len(data)):
        if data[i] % 2 == 0:
            count += 1
    
    if len(data) == 0:
        return 0.0
    else:
        return 100.0 * count / len(data)

```
{{< /details >}}
<sup><a href='https://practiceit.cs.washington.edu/problem/view/bjp5/chapter7/e10-percentEven'>source</a></sup>


<br>


### mirror

Write a function `mirror` that accepts a list as a parameter and produces a mirrors the list, with the original values followed by those same values in the opposite order. For example, if a list contained the values [‘a’, ‘b’, ‘c’], after a call to mirror; it should contain [‘a’, ‘b’, ‘c’, ‘c’, ‘b’, ‘a’]. 

```
[‘a’, ‘b’, ‘c’] ⇒ [‘a’, ‘b’, ‘c’, ‘c’, ‘b’, ‘a’] 
[5, 9, 1] ⇒ [5, 9, 1, 1, 5, 9] 
[‘a’] ⇒ [‘a’, ‘a’]
```

```python
def mirror(data):
    # Complete the function
```
{{< details title="Show Solution" open=false >}}

```python
def mirror(data):
    for i in range(len(data) - 1, -1, -1):
        data.append(data[i])
```
{{< /details >}}
<sup><a href='https://practiceit.cs.washington.edu/problem/view/bjp5/chapter10/e18-mirror'>source</a></sup>


<br>


### contains_all

Write a function called `contains_all` that accepts two lists of integers as parameters. The function returns True if every element in the first list appears at least once in the second list.

```
contains_all([-5, 0, -5, 2, -5], [2, 0, -5, 12]) ⟶ returns True 
contains_all([], [2]) ⟶ returns True 
contains_all([0, 5, 1, 17], [1, 0, 17, 17, -5, 15]) ⟶ returns False
```

```python
def contains_all(data1, data2):
    # Complete the function
```
{{< details title="Show Solution" open=false >}}

```python
def contains_all(data1, data2):
    for i in range(len(data1)):
        found = False
        j = 0
        while not found and j < len(data2):
            j += 1
            found = data1[i] == data2[j]
        if not found:
            return False
    return True
```
{{< /details >}}
<sup><a href='https://www.cs.utexas.edu/~scottm/cs312/handouts/tests/FA_19_E2.pdf'>source</a></sup>

<br>

### max_run

Complete a function that returns the length of the longest run of equal values in a list. Consecutive equal values make up a run. Consider the following example:

```python
[5, 1, 1, 5, 5, 1, 1, 2, 2, 2, 2, 3, 5]
```

The longest run of equal values is the run of four 2s shown underlined. Given the list above, the function shall return 4.

The list shall have of length greater than or equal to 1.

The only built in functions you may use are the range and len functions. Do not create any new lists. The given list is not altered by this function.

Complete the following function.

```python
# data is a list with 1 or more elements. All elements in data are integers. 
# The function returns an integer equal to the longest run of equal values 
# in data.
def max_run(data):
```
{{< details title="Show Solution" open=false >}}

```python
# data is a list with 1 or more elements. All elements in data are integers. 
# The function returns an integer equal to the longest run of equal values 
# in data.
def max_run(data):
    prev = data[0]
    run_length = 1
    max_length = 1
    for i in range(1, len(data)):
        val = data[i]
        if val == prev:
            run_length += 1
            if run_length > max_length:
                max_length = run_length
        else:
            prev = val
            run_length = 1
    return max_length
```
{{< /details >}}
<sup>source: Summer 2020 Final</sup>


<br>

### get_matching_elements

Complete a function that given two lists of Strings, returns a new list of String composed of those elements from the given two lists that have the same position, are equal ignoring case, and have a length greater than 3.

Consider this example:

```python
strs1: ['AMD',   'ibm', 'Google', 'snap', 'micro-soft', 'FACEBOOK']
strs2: ['apple', 'ibm', 'Oracle', 'Snap', 'Microsoft',  'facebook', 'AMD', 'CSC']
```

Given those two lists, the function would return the list `['snap', 'FACEBOOK']`. The relative order of the elements in the returned list is the same as in the given lists.

Notice how `ibm` is not included as it has  a length less than or equal to 3.  Note, if there is a difference in capitalization, the  string from the first list is placed in the result. `snap` instead of `Snap` for instance.

The only built in functions you may use are the len, range, and min functions, Plus the append method for lists and the lower and upper methods for strings.

Create a single list, the one that is returned by the function. The given lists are not altered by this function.

Complete the following function.

```python
# strs1 and strs2 are lists. All elements of strs1 and strs2 are strings.
def get_matching_elements(strs1, strs2):
```
{{< details title="Show Solution" open=false >}}

```python
# strs1 and strs2 are lists. All elements of strs1 and strs2 are strings.
def get_matching_elements(strs1, strs2):
    result = []
    min_length = min(len(strs1), len(strs2))
    for i in range(min_length):
        st1 = strs1[i].lower()
        st2 = strs2[i].lower()
        if len(st1) >= 4 and st1 == st2:
            result.append(strs1[i])
    return result
```
{{< /details >}}
<sup>source: Summer 2020 Final</sup>


<br>

## Multidimensional Lists


### reverse_columns

Write a function called `reverse_columns` that accepts a 2-Dimensional list as a parameter and returns a new 2-Dimensional list with each column in in the reverse order. 


$$
\text{reverse\\_columns}\left(
\begin{bmatrix}
    0 & 13 & 12 \cr
    4 & 72 & 17 \cr
    9 & 60 & 15 \cr
\end{bmatrix}\right)
\xrightarrow{returns}
\begin{bmatrix}
    9 & 60 & 15 \cr
    4 & 72 & 17 \cr
    0 & 13 & 12 \cr
\end{bmatrix}
$$

<br>
<br>

$$
\text{reverse\\_columns}\left(
\begin{bmatrix}
    0 & 1 & 2 & 3 & 4 \cr
    5 & 6 & 7 & 8 & 9  \cr
\end{bmatrix}\right)
\xrightarrow{returns}
\begin{bmatrix}
    5 & 6 & 7 & 8 & 9  \cr
    0 & 1 & 2 & 3 & 4  \cr
\end{bmatrix}
$$




```python
def reverse_columns(data):
    result = []
    # Complete the function
```
{{< details title="Show Solution" open=false >}}

```python
def reverse_columns(data):
    result = []
    for r in range(len(data)):
        result.append([])
        row_in_data = len(data) - 1 - r
        for c in range(len(data[r])):
            result[r].append(data[row_in_data][c])
    return result
```
{{< /details >}}


<br>


### swap_matrices

Write a function called `swap_matrices` that accepts two 2-Dimensional lists as parameters that have the same dimensions. An element will swap between the matrices if both the elements at the same position in the list are either both even or both odd. If just one element is even, and the other is odd, then they will stay in the same position in the same matrix.

$$
    data1=
    \begin{bmatrix}
        \bf0 & \bf13 & 12 \cr
        \bf4 & 72 & \bf17 \cr
        \bf9 & \bf60 & 15
    \end{bmatrix}
    \ \ data2=
    \begin{bmatrix}
        \bf2 & \bf19 & 21 \cr
        \bf8 & 71 & \bf19 \cr
        \bf11 & \bf22 & 26
    \end{bmatrix}
$$

<br>
<br>
$$
\text{swap\_matrices}(data1, \ data2)
$$
<br>
<br>

$$
    data1=
    \begin{bmatrix}
        \bf2 & \bf19 & 12 \cr
        \bf8 & 72 & \bf19 \cr
        \bf11 & \bf22 & 15
    \end{bmatrix}
    \ \ data2=
    \begin{bmatrix}
        \bf0 & \bf13 & 21 \cr
        \bf4 & 71 & \bf17 \cr
        \bf9 & \bf60 & 26
    \end{bmatrix}
$$

```python
def swap_evens_odds(data1, data2):
    # Complete the function
```
{{< details title="Show Solution" open=false >}}

```python
def swap_matrices(data1, data2):
    for r in range(len(data1)):
        for c in range(len(data1[r])):
            if data1[r][c] % 2 == data2[r][c] % 2:
                data1[r][c], data2[r][c] = data2[r][c], data1[r][c]
```
{{< /details >}}


<br>


### index_of_column_sum_matching_target

Complete a function that given a 2d list of integers returns the index of the column closest to 0 whose elements equal some given target value. If no column sum equals the target value return -1. Consider the following example:

```bash
[[5, 1, 8],
 [3, 0, -4],
 [-5, 3, 0]]
```
Given the above matrix, the return value for various targets would be:

```
target = 4, function returns 1
target = 3, function returns 0
target = 8, function returns -1
```

The only built in functions you may use are the range and len functions. Do not create any new lists. The given list of lists is not altered by this function.

Complete the following function.

```python
# mat is a rectangular list of lists.
# Each row has the same number of columns.
# All elements are integers.
# tgt is an integer
def index_of_column_sum_matching_target(mat, tgt):
```
{{< details title="Show Solution" open=false >}}

```python
# mat is a rectangular list of lists.
# Each row has the same number of columns.
# All elements are integers.
# tgt is an integer
def index_of_column_sum_matching_target(mat, tgt):
    for c in range(len(mat[0])):
        total = 0
        for r in range(len(mat)):
            total += mat[r][c]
        if total == tgt:
            return c
    return -1
```
{{< /details >}}
<sup>source: Summer 2020 Final</sup>


<br>

## Files

### process_file

Complete a function that given a file name, reads the lines of the file.

For each line the function prints out the number of tokens (elements separated by white space)  on the line except for the tokens that contain a given character. The average length of the tokens on the line is also printed, again excluding any tokens that contain the given character.

Example. If the given file is as follows and the target character was 'A' (tokens that are ignored are underlined):

<pre>This is line 1.
Line 2 
<u>A</u> lot of <u>Apples</u>
<u>Abba</u> <u>WAS</u> <u>Awestruck</u> 
a lot of apples
</pre>

Then the output of the function would be:

<pre>line 1 tokens 4 average length: 3.0
line 2 tokens 2 average length: 2.5
line 3 tokens 2 average length: 2.5
line 4 no tokens
line 5 tokens 4 average length: 3.0
</pre>

The only built in functions you may use are the open, len, and print, plus the readlines method for file objects and the split method for strings.

Complete the following function. Do not repeat the function header in your answer.

```python
# file_name is the name of a file that exists. 
# tgt_ch is a string consisting of a single character.
def process_file(file_name, tgt_ch):
```
{{< details title="Show Solution" open=false >}}

```python
# file_name is the name of a file that exists. 
# tgt_ch is a string consisting of a single character.
def process_file(file_name, tgt_ch):
    infile = open(file_name)
    line_num = 1
    for line in infile.readlines():
        num = 0
        total_length = 0
        for token in line.split():
            if not tgt_ch in token:
                num += 1
                total_length += len(token)
        if num != 0:
            print('line', line_num, 'tokens', num, 'average length:',
                  (total_length / num))
        else:
            print('line', line_num, 'no tokens')
        line_num += 1
```
{{< /details >}}
<sup>source: Summer 2020 Final</sup>


<br>


## Dictionaries

### update_authors

Complete a function that given a dictionary showing collaborations between authors of academic papers and a list of Strings of the co-authors for a new paper, updates the dictionary.

Modern academic papers typically have multiple authors. For example, here are the authors of recent paper by UTCS's own William Cook:

![](/~bebeal/coding-questions_/dict1.png)

The dictionary sent to this function has keys that are strings, the last names of authors. The values in the dictionary are also dictionaries. The value dictionaries have keys that are strings representing the co-authors of the given author from the original dictionary. The values of the sub dictionary are integers, the number of times the two authors have been co-authors.

For example, the initial dictionary might look something like this (quotes on strings not shown):


|key|value (a sub dictionary)|
|---|------------------------|
Loh|	{Cook: 2, Miller: 1, Lee: 3}|
Cook|	{Loh: 2, Lee: 5}|
Lee|	{Loh: 3, Cook: 5}|
Miller|	{Loh: 1}|

The author list for the paper shown above would be `['Storm', 'Cook', 'Loh']`

The function updates the dictionary based on the author list for the paper. After the function the dictionary for this example would be as follows (quotes on strings not shown):


|key	| value (a sub dictionary)|
|---|---|
Loh|{Cook: 3, Miller: 1, Lee: 3, Storm: 1}|
Cook|	{Loh: 2, Lee: 5, Storm: 1}|
Lee|	{Loh: 3, Cook: 5}|
Miller|	{Loh: 1}|
Storm|	{Cook: 1, Loh: 1}|

You may assume none of the authors of a paper have the same last name.

Do not use any built in functions. Do not create any data structures other than new sub dictionaries for authors that did not appear in the main dictionary before the function call.

Complete the following function.

```python
# authors is a dictionary as described in the question.
# paper is  a list of Strings with no duplicate elements.
def update_authors(authors, paper):
```
{{< details title="Show Solution" open=false >}}

```python
# authors is a dictionary as described in the question.
# paper is  a list of Strings with no duplicate elements.
def update_authors(authors, paper):
    for author in paper:
        sub = {}
        if author in authors:
            sub = authors[author]
        else:
            authors[author] = sub
        for coauthor in paper:
            if coauthor != author:
                if coauthor in sub:
                    sub[coauthor] += 1
                else:
                    sub[coauthor] = 1
```
{{< /details >}}
<sup>source: Summer 2020 Final</sup>


<br>

{{<katex>}}
{{</katex>}}