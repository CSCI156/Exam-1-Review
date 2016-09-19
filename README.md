1 
```
s = "23" + "!@" + "alm"
```
What is the value of s?

2 
```
s = s + "3"
```
Is this a proper one line program?

3
What is the output of the following program?
```
x = 3
y = 2.0
s = "2"
x = x + 5
y += 5
s += " is better than 1"
print(x, y, s)
```

4
```
def add_two(x):
    print(x+2)

add_two(1)
add_two(2)
add_two(3)
add_two(4)
add_two(5)
add_two(6)
```
    a. What is the output of this program?
    b. Rewrite the program removing the 6 add_two calls and replacing it with a single for loop.

5 What is the output of the following program?
```
def local_vs_global():
    global x
    x = 3
    y = 4
    print(x, y) 
    
x = 1
y = 2
print(x, y)
local_vs_global()
print(x, y)
```

6 What is the output of the following programs? You should be able to trace these using a table.
```
x = 5
for i in range(10):
    x = x + 2
print(x)
```
```
x = 5
for i in range(10):
    x = x + i
    print(x)
```
```
x = 5
for i in range(10):
    x = x + i*x
print(x)
```

7 What is the output of the following programs? You should be able to trace these using a table.
```
def looper(x):
    for i in range(6):
        print(i)
        
looper(20)
```
```
def looper2(x)
    for i in range(6):
        print(x)

looper2(20)
```
```
def looper3(x)
    y = 1 
    s = "1"
    for i in range(2,x):
        print(s + " = " + str(y))
        y = y * i
        s = s + "*" + str(i)

looper3(4)
```

8 What about the following code is not a good idea?
```
def not_a_good_idea(x):
    x = 1
    print(x)
```
```
def not_a_good_idea2(x):
    for i in range(x):
        i = i * 2
        print(i)
```
```
def not_a_good_idea2(x):
    t = 0
    for i in range(x):
        t += 2
    print(x)
```

9 Write a program the will build the string "1+2+3+4+5" using a for loop. It should not have a leading or following "+".

10 Write a procedure that will add the first n perfect squares.

11 What is the output of the following program?
```
x = 0
for i in range(10):
    if i==1 or i==5:
        x += i
    elif i==3 or i==7:
        x += i**2
    elif i==3 or i==9:
        x += 2
    else:
        x += 4
print(x)
```

12 Write a procedure that prints out "even" if the parameter has a value from 0 to 10 and is an even number, prints out "odd" if the parameter has a value from 0 to 10 and is odd, otherwise it prints out "Out of range.".



## Things you should know
- What is the difference between a string, an integer, and a float?
- What is the difference between = and == ?
- What do the following ranges give?
  range(m)
  range(m, n)
  range(m, n, 2)
- What do if, elif, and else mean?
- How to input a variable.
- What does += do?
- What do str() and int() do?
- How to trace a program by hand, especially a program that has a loop.
- What is a parameter?




#### Answers
1 
```
"23!@alm"
```

2 No, if that is the only line of code the interpreter has no way of knowing what s is, and therefore cannot add "3" to it. You will get an error.

3 
```
8 7.0 2 is better than 1
```

4
```
3
4
5
6
7
8
```
```
def add_two(x)
    print(x+2)
    
for i in range(1,7):
    add_two(i)
```

5
```
1 2
3 4
3 2
```

6
```
25
```
```

