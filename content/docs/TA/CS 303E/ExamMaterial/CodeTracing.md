---
weight: 20
title: Code Tracing
---
# Code Tracing Problems

---

<script>
    function submitAnswer(number, answer) {
        var answer = document.getElementById("A" + number + "_" + answer);
        if (answer.checked) {
            document.getElementById("result" + number).innerHTML = " Correct!";
            var rest = document.getElementsByName("Q" + number);
            for (i = 0; i < rest.length; i++){
                rest[i].disabled = true;
            }
            document.getElementById("submit" + number).style.display='none';
        } else {
            document.getElementById("result" + number).innerHTML = " Incorrect";
        }
    }
</script>






## Math Functions and Operations

<div>
1. What is output by the following code
</div>

```python
x = int(52.2)
y = math.floor(999.9)
print(x, y)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A1_1_0" name="Q1_1">
        <label for="A1_1_0">{{< highlight python >}}52.0 999.0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_1_1" name="Q1_1">
        <label for="A1_1_1">{{< highlight python >}}52 999{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_1_2" name="Q1_1">
        <label for="A1_1_2">{{< highlight python >}}52.0 1000.0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_1_3" name="Q1_1">
        <label for="A1_1_3">{{< highlight python >}}52 1000{{< / highlight >}}</label>
    </div>
<br>
<button id="submit1_1" onclick="submitAnswer('1_1', 1)">submit</button>
<div id="result1_1" style="display:inline;"></div>
</div><br>

<div>
2. What is output by the following code
</div>

```python
t = math.floor(-909.1)
a = int(-49.1)
print(t, a)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A1_2_0" name="Q1_2">
        <label for="A1_2_0">{{< highlight python >}}-909 -50{{< / highlight >}}</label>
    </div>
    <div class="inputGroup">
        <input type="radio" id="A1_2_1" name="Q1_2">
        <label for="A1_2_1">{{< highlight python >}}-908 -50{{< / highlight >}}</label>
    </div>
    <div class="inputGroup">
        <input type="radio" id="A1_2_2" name="Q1_2">
        <label for="A1_2_2">{{< highlight python >}}-910 -49{{< / highlight >}}</label>
    </div>
    <div class="inputGroup">
        <input type="radio" id="A1_2_3" name="Q1_2">
        <label for="A1_2_3">{{< highlight python >}}-908 -49{{< / highlight >}}</label>
    </div>
    <div class="inputGroup">
        <input type="radio" id="A1_2_4" name="Q1_2">
        <label for="A1_2_4">{{< highlight python >}}-909 -49{{< / highlight >}}</label>
    </div>
    <div class="inputGroup">
        <input type="radio" id="A1_2_5" name="Q1_2">
        <label for="A1_2_5">{{< highlight python >}}-910 -50{{< / highlight >}}</label>
    </div>
<br>
<button id="submit1_2" onclick="submitAnswer('1_2', 2)">submit</button>
<div id="result1_2" style="display:inline;"></div>
</div><br>

<div>
3. What is output by the following code
</div>

```python
y = math.floor(-3.99 - .01)
j = math.floor(5.99 + .1)
print(y, j)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A1_3_0" name="Q1_3">
        <label for="A1_3_0">{{< highlight python >}}-4 6{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_3_1" name="Q1_3">
        <label for="A1_3_1">{{< highlight python >}}-3 5{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_3_2" name="Q1_3">
        <label for="A1_3_2">{{< highlight python >}}RUNTIME ERROR{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_3_3" name="Q1_3">
        <label for="A1_3_3">{{< highlight python >}}-4 5{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_3_4" name="Q1_3">
        <label for="A1_3_4">{{< highlight python >}}-3 6{{< / highlight >}}</label>
    </div>
<br>
<button id="submit1_3" onclick="submitAnswer('1_3', 0)">submit</button>
<div id="result1_3" style="display:inline;"></div>
</div><br>

<div>
4. What is output by the following code
</div>

```python
m = int(52.9 + .1)
print(m)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A1_4_0" name="Q1_4">
        <label for="A1_4_0">{{< highlight python >}}53.0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_4_1" name="Q1_4">
        <label for="A1_4_1">{{< highlight python >}}52.0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_4_2" name="Q1_4">
        <label for="A1_4_2">{{< highlight python >}}53{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_4_3" name="Q1_4">
        <label for="A1_4_3">{{< highlight python >}}52{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_4_4" name="Q1_4">
        <label for="A1_4_4">{{< highlight python >}}RUNTIME ERROR{{< / highlight >}}</label>
    </div>
<br>
<button id="submit1_4" onclick="submitAnswer('1_4', 2)">submit</button>
<div id="result1_4" style="display:inline;"></div>
</div><br>

<div>
5. What is output by the following code
</div>

```python
p = 10 // 3
q = 3 // 10
print(p, q)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A1_5_0" name="Q1_5">
        <label for="A1_5_0">{{< highlight python >}}3.0 3.0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_5_1" name="Q1_5">
        <label for="A1_5_1">{{< highlight python >}}3 0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_5_2" name="Q1_5">
        <label for="A1_5_2">{{< highlight python >}}3.0 0.0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_5_3" name="Q1_5">
        <label for="A1_5_3">{{< highlight python >}}3 3{{< / highlight >}}</label>
    </div>
<br>
<button id="submit1_5" onclick="submitAnswer('1_5', 1)">submit</button>
<div id="result1_5" style="display:inline;"></div>
</div><br>

<div>
6. What is output by the following code
</div>

```python
y = 4 / 2
a = 2 % 6
print(y, a)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A1_6_0" name="Q1_6">
        <label for="A1_6_0">{{< highlight python >}}2 2{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_6_1" name="Q1_6">
        <label for="A1_6_1">{{< highlight python >}}2.0 0.0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_6_2" name="Q1_6">
        <label for="A1_6_2">{{< highlight python >}}2.0 2{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_6_3" name="Q1_6">
        <label for="A1_6_3">{{< highlight python >}}2.0 2.0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_6_4" name="Q1_6">
        <label for="A1_6_4">{{< highlight python >}}2 0{{< / highlight >}}</label>
    </div>
<br>
<button id="submit1_6" onclick="submitAnswer('1_6', 2)">submit</button>
<div id="result1_6" style="display:inline;"></div>
</div><br>

<div>
7. What is output by the following code
</div>

```python
f = 9 % -4
g = -7 % 13
print(f, g)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A1_7_0" name="Q1_7">
        <label for="A1_7_0">{{< highlight python >}}-3 -6{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_7_1" name="Q1_7">
        <label for="A1_7_1">{{< highlight python >}}-1 -7{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_7_2" name="Q1_7">
        <label for="A1_7_2">{{< highlight python >}}1 -7{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_7_3" name="Q1_7">
        <label for="A1_7_3">{{< highlight python >}}-3 6{{< / highlight >}}</label>
    </div>
<br>
<button id="submit1_7" onclick="submitAnswer('1_7', 3)">submit</button>
<div id="result1_7" style="display:inline;"></div>
</div><br>

<div>
8. What is output by the following code
</div>

```python
x = 2
y = x - 2
x *= 2
y += -1
print(x, y)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A1_8_0" name="Q1_8">
        <label for="A1_8_0">{{< highlight python >}}4 1{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_8_1" name="Q1_8">
        <label for="A1_8_1">{{< highlight python >}}4 -1{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_8_2" name="Q1_8">
        <label for="A1_8_2">{{< highlight python >}}0 1{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_8_3" name="Q1_8">
        <label for="A1_8_3">{{< highlight python >}}0 -1{{< / highlight >}}</label>
    </div>
<br>
<button id="submit1_8" onclick="submitAnswer('1_8', 1)">submit</button>
<div id="result1_8" style="display:inline;"></div>
</div><br>

<div>
9. What is output by the following code
</div>

```python
x = int(-4.2 * 2)
print(x)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A1_9_0" name="Q1_9">
        <label for="A1_9_0">{{< highlight python >}}-8{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_9_1" name="Q1_9">
        <label for="A1_9_1">{{< highlight python >}}-8.4{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_9_2" name="Q1_9">
        <label for="A1_9_2">{{< highlight python >}}-9{{< / highlight >}}</label>
    </div>
<br>
<button id="submit1_9" onclick="submitAnswer('1_9', 0)">submit</button>
<div id="result1_9" style="display:inline;"></div>
</div><br>

<div>
10. What is output by the following code
</div>

```python
x = 2.0
y = 3.0
z = 2.0
y *= z % (x + y)
print(y, z)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A1_10_0" name="Q1_10">
        <label for="A1_10_0">{{< highlight python >}}6 2{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_10_1" name="Q1_10">
        <label for="A1_10_1">{{< highlight python >}}6.0 2.0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_10_2" name="Q1_10">
        <label for="A1_10_2">{{< highlight python >}}1.0 2.0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_10_3" name="Q1_10">
        <label for="A1_10_3">{{< highlight python >}}1 2{{< / highlight >}}</label>
    </div>
<br>
<button id="submit1_10" onclick="submitAnswer('1_10', 1)">submit</button>
<div id="result1_10" style="display:inline;"></div>
</div><br>

<div>
11. What is output by the following code
</div>

```python
x = 112 % 100 + 2 % 10
y = 1.0 // x
print(x, y)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A1_11_0" name="Q1_11">
        <label for="A1_11_0">{{< highlight python >}}14 0.0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_11_1" name="Q1_11">
        <label for="A1_11_1">{{< highlight python >}}14 0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_11_2" name="Q1_11">
        <label for="A1_11_2">{{< highlight python >}}4 0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A1_11_3" name="Q1_11">
        <label for="A1_11_3">{{< highlight python >}}4 1.0{{< / highlight >}}</label>
    </div>
<br>
<button id="submit1_11" onclick="submitAnswer('1_11', 0)">submit</button>
<div id="result1_11" style="display:inline;"></div>
</div><br>






## Built-In Functions

<div>
1. What is output by the following code
</div>

```python
x = eval('4')
y = int('-23')
print(y, x)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A2_1_0" name="Q2_1">
        <label for="A2_1_0">{{< highlight python >}}RUNTIME ERROR{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_1_1" name="Q2_1">
        <label for="A2_1_1">{{< highlight python >}}4 -23{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_1_2" name="Q2_1">
        <label for="A2_1_2">{{< highlight python >}}23 -4{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_1_3" name="Q2_1">
        <label for="A2_1_3">{{< highlight python >}}-23 4{{< / highlight >}}</label>
    </div>
<br>
<button id="submit2_1" onclick="submitAnswer('2_1', 3)">submit</button>
<div id="result2_1" style="display:inline;"></div>
</div><br>

<div>
2. What is output by the following code
</div>

```python
a = eval('9 + 1')
print(a)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A2_2_0" name="Q2_2">
        <label for="A2_2_0">{{< highlight python >}}9 + 1{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_2_1" name="Q2_2">
        <label for="A2_2_1">{{< highlight python >}}RUNTIME ERROR{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_2_2" name="Q2_2">
        <label for="A2_2_2">{{< highlight python >}}10{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_2_3" name="Q2_2">
        <label for="A2_2_3">{{< highlight python >}}10.0{{< / highlight >}}</label>
    </div>
<br>
<button id="submit2_2" onclick="submitAnswer('2_2', 2)">submit</button>
<div id="result2_2" style="display:inline;"></div>
</div><br>

<div>
3. What is output by the following code
</div>

```python
t = int('1 - 1')
print(t)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A2_3_0" name="Q2_3">
        <label for="A2_3_0">{{< highlight python >}}RUNTIME ERROR{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_3_1" name="Q2_3">
        <label for="A2_3_1">{{< highlight python >}}1 - 1{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_3_2" name="Q2_3">
        <label for="A2_3_2">{{< highlight python >}}0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_3_3" name="Q2_3">
        <label for="A2_3_3">{{< highlight python >}}0.0{{< / highlight >}}</label>
    </div>
<br>
<button id="submit2_3" onclick="submitAnswer('2_3', 0)">submit</button>
<div id="result2_3" style="display:inline;"></div>
</div><br>

<div>
4. What is output by the following code
</div>

```python
k = eval('99.0 + 1')
print(k)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A2_4_0" name="Q2_4">
        <label for="A2_4_0">{{< highlight python >}}100.0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_4_1" name="Q2_4">
        <label for="A2_4_1">{{< highlight python >}}RUNTIME ERROR{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_4_2" name="Q2_4">
        <label for="A2_4_2">{{< highlight python >}}100{{< / highlight >}}</label>
    </div>
<br>
<button id="submit2_4" onclick="submitAnswer('2_4', 0)">submit</button>
<div id="result2_4" style="display:inline;"></div>
</div><br>

<div>
5. What is output by the following code
</div>

```python
x = min(max(3, 6), max(4, 7))
print(x)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A2_5_0" name="Q2_5">
        <label for="A2_5_0">{{< highlight python >}}4{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_5_1" name="Q2_5">
        <label for="A2_5_1">{{< highlight python >}}6{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_5_2" name="Q2_5">
        <label for="A2_5_2">{{< highlight python >}}6 7{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A2_5_3" name="Q2_5">
        <label for="A2_5_3">{{< highlight python >}}7{{< / highlight >}}</label>
    </div>
<br>
<button id="submit2_5" onclick="submitAnswer('2_5', 1)">submit</button>
<div id="result2_5" style="display:inline;"></div>
</div><br>


## Booleans and Conditionals

<div>
1. What is output by the following code
</div>

```python
x = 2
y = 4
z = 9
if x <= 2 and y > 4:
    print('case1')
elif z < 9 or x >= 2:
    print('case2')
else:
    print('case3')
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A3_1_0" name="Q3_1">
        <label for="A3_1_0">{{< highlight python >}}case1{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_1_1" name="Q3_1">
        <label for="A3_1_1">{{< highlight python >}}case3{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_1_2" name="Q3_1">
        <label for="A3_1_2">{{< highlight python >}}case2{{< / highlight >}}</label>
    </div>
<br>
<button id="submit3_1" onclick="submitAnswer('3_1', 2)">submit</button>
<div id="result3_1" style="display:inline;"></div>
</div><br>

<div>
2. What is output by the following code
</div>

```python
count = 0
x = 'A'
y = 'B'
if x == 'X' or y == x:
    count += 1
elif count < 50 and y == 'B':
    count += 5
else:
    count *= 3
count *= 2
print(count)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A3_2_0" name="Q3_2">
        <label for="A3_2_0">{{< highlight python >}}8{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_2_1" name="Q3_2">
        <label for="A3_2_1">{{< highlight python >}}10{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_2_2" name="Q3_2">
        <label for="A3_2_2">{{< highlight python >}}1{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_2_3" name="Q3_2">
        <label for="A3_2_3">{{< highlight python >}}5{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_2_4" name="Q3_2">
        <label for="A3_2_4">{{< highlight python >}}2{{< / highlight >}}</label>
    </div>
<br>
<button id="submit3_2" onclick="submitAnswer('3_2', 1)">submit</button>
<div id="result3_2" style="display:inline;"></div>
</div><br>

<div>
3. What is output by the following code
</div>

```python
num = random.randint(0,1)
if num == 0:
    print(num)
elif num == 1:
    print(num - 1)
else:
    print(50)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A3_3_0" name="Q3_3">
        <label for="A3_3_0">{{< highlight python >}}0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_3_1" name="Q3_3">
        <label for="A3_3_1">{{< highlight python >}}Impossible to Determine{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_3_2" name="Q3_3">
        <label for="A3_3_2">{{< highlight python >}}50{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_3_3" name="Q3_3">
        <label for="A3_3_3">{{< highlight python >}}1{{< / highlight >}}</label>
    </div>
<br>
<button id="submit3_3" onclick="submitAnswer('3_3', 0)">submit</button>
<div id="result3_3" style="display:inline;"></div>
</div><br>

<div>
4. What is output by the following code
</div>

```python
x = 1
y = '1'
a = x == y and x > 0
b = y != '1' or x % 5 >= 1
print(a, b)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A3_4_0" name="Q3_4">
        <label for="A3_4_0">{{< highlight python >}}True True{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_4_1" name="Q3_4">
        <label for="A3_4_1">{{< highlight python >}}True False{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_4_2" name="Q3_4">
        <label for="A3_4_2">{{< highlight python >}}False False{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_4_3" name="Q3_4">
        <label for="A3_4_3">{{< highlight python >}}False True{{< / highlight >}}</label>
    </div>
<br>
<button id="submit3_4" onclick="submitAnswer('3_4', 3)">submit</button>
<div id="result3_4" style="display:inline;"></div>
</div><br>

<div>
5. What is output by the following code
</div>

```python
x = random.randint(5, 10)
y = x == 7 or not '1' == 1
z = 42
a = y and z > x
print(y, a)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A3_5_0" name="Q3_5">
        <label for="A3_5_0">{{< highlight python >}}True True{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_5_1" name="Q3_5">
        <label for="A3_5_1">{{< highlight python >}}True False{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_5_2" name="Q3_5">
        <label for="A3_5_2">{{< highlight python >}}False False{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_5_3" name="Q3_5">
        <label for="A3_5_3">{{< highlight python >}}Impossible to determine{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_5_4" name="Q3_5">
        <label for="A3_5_4">{{< highlight python >}}False True{{< / highlight >}}</label>
    </div>
<br>
<button id="submit3_5" onclick="submitAnswer('3_5', 0)">submit</button>
<div id="result3_5" style="display:inline;"></div>
</div><br>

<div>
6. What is output by the following code
</div>

```python
x = 501
y = 500
z = 5
p = y % z == 0 and not (y + z > x or x // z == 0)
q = not (z > x - y and x % y == 1)
print(p, q)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A3_6_0" name="Q3_6">
        <label for="A3_6_0">{{< highlight python >}}True False{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_6_1" name="Q3_6">
        <label for="A3_6_1">{{< highlight python >}}False False{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_6_2" name="Q3_6">
        <label for="A3_6_2">{{< highlight python >}}False True{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A3_6_3" name="Q3_6">
        <label for="A3_6_3">{{< highlight python >}}True True{{< / highlight >}}</label>
    </div>
<br>
<button id="submit3_6" onclick="submitAnswer('3_6', 1)">submit</button>
<div id="result3_6" style="display:inline;"></div>
</div><br>







## Iteration

<div>
1. What is output by the following code
</div>

```python
count = 0
for i in range(0, 10):
    count *= 2
print(count)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A4_1_0" name="Q4_1">
        <label for="A4_1_0">{{< highlight python >}}2{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_1_1" name="Q4_1">
        <label for="A4_1_1">{{< highlight python >}}1024{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_1_2" name="Q4_1">
        <label for="A4_1_2">{{< highlight python >}}0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_1_3" name="Q4_1">
        <label for="A4_1_3">{{< highlight python >}}20{{< / highlight >}}</label>
    </div>
<br>
<button id="submit4_1" onclick="submitAnswer('4_1', 2)">submit</button>
<div id="result4_1" style="display:inline;"></div>
</div><br>

<div>
2. What is output by the following code
</div>

```python
loop_control = 1
count = 0
while loop_control < 10:
    loop_control *= 2
    count += 1
print(count)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A4_2_0" name="Q4_2">
        <label for="A4_2_0">{{< highlight python >}}6{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_2_1" name="Q4_2">
        <label for="A4_2_1">{{< highlight python >}}5{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_2_2" name="Q4_2">
        <label for="A4_2_2">{{< highlight python >}}4{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_2_3" name="Q4_2">
        <label for="A4_2_3">{{< highlight python >}}3{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_2_4" name="Q4_2">
        <label for="A4_2_4">{{< highlight python >}}10{{< / highlight >}}</label>
    </div>
<br>
<button id="submit4_2" onclick="submitAnswer('4_2', 2)">submit</button>
<div id="result4_2" style="display:inline;"></div>
</div><br>

<div>
3. What is output by the following code
</div>

```python
what_am_i = 0
for i in range(50):
    what_am_i = i
print(what_am_i)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A4_3_0" name="Q4_3">
        <label for="A4_3_0">{{< highlight python >}}1{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_3_1" name="Q4_3">
        <label for="A4_3_1">{{< highlight python >}}50{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_3_2" name="Q4_3">
        <label for="A4_3_2">{{< highlight python >}}RUNTIME ERROR{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_3_3" name="Q4_3">
        <label for="A4_3_3">{{< highlight python >}}49{{< / highlight >}}</label>
    </div>
<br>
<button id="submit4_3" onclick="submitAnswer('4_3', 3)">submit</button>
<div id="result4_3" style="display:inline;"></div>
</div><br>

<div>
4. What is output by the following code
</div>

```python
loop_control = -2
while loop_control < 50:
    loop_control += 1
print(loop_control)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A4_4_0" name="Q4_4">
        <label for="A4_4_0">{{< highlight python >}}48{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_4_1" name="Q4_4">
        <label for="A4_4_1">{{< highlight python >}}49{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_4_2" name="Q4_4">
        <label for="A4_4_2">{{< highlight python >}}51{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_4_3" name="Q4_4">
        <label for="A4_4_3">{{< highlight python >}}50{{< / highlight >}}</label>
    </div>
<br>
<button id="submit4_4" onclick="submitAnswer('4_4', 3)">submit</button>
<div id="result4_4" style="display:inline;"></div>
</div><br>

<div>
5. What is output by the following code
</div>

```python
count = 0
for i in range(3, 15, 3):
    count += 2
print(count)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A4_5_0" name="Q4_5">
        <label for="A4_5_0">{{< highlight python >}}12{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_5_1" name="Q4_5">
        <label for="A4_5_1">{{< highlight python >}}3{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_5_2" name="Q4_5">
        <label for="A4_5_2">{{< highlight python >}}8{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_5_3" name="Q4_5">
        <label for="A4_5_3">{{< highlight python >}}4{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_5_4" name="Q4_5">
        <label for="A4_5_4">{{< highlight python >}}15{{< / highlight >}}</label>
    </div>
<br>
<button id="submit4_5" onclick="submitAnswer('4_5', 2)">submit</button>
<div id="result4_5" style="display:inline;"></div>
</div><br>

<div>
6. What is output by the following code
</div>

```python
loop_control = -10
while loop_control <= 0:
    loop_control *= 2
print(loop_control)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A4_6_0" name="Q4_6">
        <label for="A4_6_0">{{< highlight python >}}0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_6_1" name="Q4_6">
        <label for="A4_6_1">{{< highlight python >}}INFINITE LOOP{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_6_2" name="Q4_6">
        <label for="A4_6_2">{{< highlight python >}}1{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_6_3" name="Q4_6">
        <label for="A4_6_3">{{< highlight python >}}20{{< / highlight >}}</label>
    </div>
<br>
<button id="submit4_6" onclick="submitAnswer('4_6', 1)">submit</button>
<div id="result4_6" style="display:inline;"></div>
</div><br>

<div>
7. What is output by the following code
</div>

```python
count = 0
for i in range(10, 0, -1):
    count += 1
print(count)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A4_7_0" name="Q4_7">
        <label for="A4_7_0">{{< highlight python >}}9{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_7_1" name="Q4_7">
        <label for="A4_7_1">{{< highlight python >}}10{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_7_2" name="Q4_7">
        <label for="A4_7_2">{{< highlight python >}}0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_7_3" name="Q4_7">
        <label for="A4_7_3">{{< highlight python >}}INFINITE LOOP{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_7_4" name="Q4_7">
        <label for="A4_7_4">{{< highlight python >}}11{{< / highlight >}}</label>
    </div>
<br>
<button id="submit4_7" onclick="submitAnswer('4_7', 1)">submit</button>
<div id="result4_7" style="display:inline;"></div>
</div><br>

<div>
8. What is output by the following code
</div>

```python
count = 0
for i in range(7):
    for j in range(2):
        count += j
print(count)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A4_8_0" name="Q4_8">
        <label for="A4_8_0">{{< highlight python >}}2{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_8_1" name="Q4_8">
        <label for="A4_8_1">{{< highlight python >}}14{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_8_2" name="Q4_8">
        <label for="A4_8_2">{{< highlight python >}}7{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A4_8_3" name="Q4_8">
        <label for="A4_8_3">{{< highlight python >}}21{{< / highlight >}}</label>
    </div>
<br>
<button id="submit4_8" onclick="submitAnswer('4_8', 2)">submit</button>
<div id="result4_8" style="display:inline;"></div>
</div><br>








## Functions

<div>
1. What is output by the following code
</div>

```python
def a(x, y):
    x = 3
    y = 3
    return x * y
def b(z, t):
    z += 2
    t = a(z, t)
    return z * t
what_am_i = b(0, 0)
print(what_am_i)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A5_1_0" name="Q5_1">
        <label for="A5_1_0">{{< highlight python >}}18{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A5_1_1" name="Q5_1">
        <label for="A5_1_1">{{< highlight python >}}11{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A5_1_2" name="Q5_1">
        <label for="A5_1_2">{{< highlight python >}}9{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A5_1_3" name="Q5_1">
        <label for="A5_1_3">{{< highlight python >}}0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A5_1_4" name="Q5_1">
        <label for="A5_1_4">{{< highlight python >}}2{{< / highlight >}}</label>
    </div>
<br>
<button id="submit5_1" onclick="submitAnswer('5_1', 0)">submit</button>
<div id="result5_1" style="display:inline;"></div>
</div><br>

<div>
2. What is output by the following code
</div>

```python
def a(x):
    x = b(x)
    return x + 2
def b(y):
    return y * 2
what_am_i = a(5)
print(what_am_i)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A5_2_0" name="Q5_2">
        <label for="A5_2_0">{{< highlight python >}}7{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A5_2_1" name="Q5_2">
        <label for="A5_2_1">{{< highlight python >}}12{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A5_2_2" name="Q5_2">
        <label for="A5_2_2">{{< highlight python >}}9{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A5_2_3" name="Q5_2">
        <label for="A5_2_3">{{< highlight python >}}10{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A5_2_4" name="Q5_2">
        <label for="A5_2_4">{{< highlight python >}}0{{< / highlight >}}</label>
    </div>
<br>
<button id="submit5_2" onclick="submitAnswer('5_2', 1)">submit</button>
<div id="result5_2" style="display:inline;"></div>
</div><br>

<div>
3. What is output by the following code
</div>

```python
def a(x, y):
    return x + y
def b(z, t):
    z = 0
    t = 1
    return a(z, t)
z = 50
t = 0
print(b(z, t), z, t)
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A5_3_0" name="Q5_3">
        <label for="A5_3_0">{{< highlight python >}}50 50 0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A5_3_1" name="Q5_3">
        <label for="A5_3_1">{{< highlight python >}}1 50 0{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A5_3_2" name="Q5_3">
        <label for="A5_3_2">{{< highlight python >}}1 0 1{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A5_3_3" name="Q5_3">
        <label for="A5_3_3">{{< highlight python >}}50 0 1{{< / highlight >}}</label>
    </div>
<br>
<button id="submit5_3" onclick="submitAnswer('5_3', 1)">submit</button>
<div id="result5_3" style="display:inline;"></div>
</div><br>



## Classes and Objects

Use the class below to answer the following questions

```python
class Car:
    def __init__(self, type_of_car, color, gas_tank_capacity=15):
        self.type_of_car = type_of_car
        self.color = color
        self.gas_tank_capacity = gas_tank_capacity
        self.num_gallons = 0

    def paint_job(self, new_color):
        self.color = new_color

    def drive(self, num_miles):
        self.num_gallons -= num_miles
        return self.num_gallons

    def fill_up(self, gallons):
        self.num_gallons += gallons
        if self.num_gallons > self.gas_tank_capacity:
            self.num_gallons = self.gas_tank_capacity
        return self.num_gallons

    def get_info(self):
        return self.color + ' ' + self.type_of_car

    def add_capacity(self, new_capacity):
        gas_tank_capacity = new_capacity
```

<br>


<div>
1. What is output by the following code
</div>

```python
e_type = Car('Jaguar E-Type', 'Black', 17)
print(e_type.fill_up(20))
print(e_type.drive(10))
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A9_1_0" name="Q9_1">
        <label for="A9_1_0">{{< highlight python >}}RUNTIME ERROR{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A9_1_1" name="Q9_1">
        <label for="A9_1_1">{{< highlight python >}}20{{< / highlight >}}{{< highlight python >}}10{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A9_1_2" name="Q9_1">
        <label for="A9_1_2">{{< highlight python >}}17{{< / highlight >}}{{< highlight python >}}7{{< / highlight >}}</label>
    </div>
<br>
<button id="submit9_1" onclick="submitAnswer('9_1', 2)">submit</button>
<div id="result9_1" style="display:inline;"></div>
</div><br>

<div>
2. What is output by the following code
</div>

```python
roadster = Car('Tesla Roadster', 'Red', 999)
print(roadster.get_info())
roadster.paint_job('Blue')
print(roadster.get_info())
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A9_2_0" name="Q9_2">
        <label for="A9_2_0">{{< highlight python >}}RUNTIME ERROR{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A9_2_1" name="Q9_2">
        <label for="A9_2_1">{{< highlight python >}}Red Tesla Roadster{{< / highlight >}}{{< highlight python >}}Blue Tesla Roadster{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A9_2_2" name="Q9_2">
        <label for="A9_2_2">{{< highlight python >}}Red Tesla Roadster{{< / highlight >}}{{< highlight python >}}Red Tesla Roadster{{< / highlight >}}</label>
    </div>
<br>
<button id="submit9_2" onclick="submitAnswer('9_2', 1)">submit</button>
<div id="result9_2" style="display:inline;"></div>
</div><br>

<div>
3. What is output by the following code
</div>

```python
lemon = Car('Lemon', 'Brown', 0)
lemon.add_capacity(1000)
print(lemon.fill_up(100))
print(lemon.drive(10))
```

<div class=question>
    <div class="inputGroup">
        <input type="radio" id="A9_3_0" name="Q9_3">
        <label for="A9_3_0">{{< highlight python >}}0{{< / highlight >}}{{< highlight python >}}-10{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A9_3_1" name="Q9_3">
        <label for="A9_3_1">{{< highlight python >}}RUNTIME ERROR{{< / highlight >}}</label>
    </div>
<div class="inputGroup">
        <input type="radio" id="A9_3_2" name="Q9_3">
        <label for="A9_3_2">{{< highlight python >}}100{{< / highlight >}}{{< highlight python >}}90{{< / highlight >}}</label>
    </div>
<br>
<button id="submit9_3" onclick="submitAnswer('9_3', 0)">submit</button>
<div id="result9_3" style="display:inline;"></div>
</div><br>