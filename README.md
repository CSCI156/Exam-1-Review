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

looper3(6)
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
def not_a_good_idea3(x):
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
Trace:
x = 5
i| x
____
0| 7
1| 9
2| 11
3| 13
4| 15
5| 17
6| 19
7| 21
8| 23
9| 25

Output: 25
```
```
Trace:
x = 5
i| x
____
0| 5
1| 6
2| 8
3| 11
4| 15
5| 20
6| 26
7| 33
8| 41
9| 50

Output:
5
6
8
11
15
20
26
33
41
50
```
```
Trace:
x = 5
i| x
____
0| 5
1| 5 + 1*5 = 10
2| 10 + 2*10 = 30
3| 30 + 3*30 = 120
4| 120 + 4*120 = 600
5| 600 + 5*600 = 3,600
6| 3600 + 6*3600 = 25,200
7| 25200 + 7*25200 = 201,600
8| 201600 + 8*201600 = 1,814,400
9| 1814400 + 9*1814400 = 18,144,000

Output: 
18144000
```

7
```
0
1
2
3
4
5
```
```
20
20
20
20
20
20
```
```
Trace:

i| y   | s
_______________
2| 2   |"1*2"
3| 6   |"1*2*3"
4| 24  |"1*2*3*4"
5| 120 |"1*2*3*4*5"

Output:
1 = 1
1*2 = 2
1*2*3 = 6
1*2*3*4 = 24
```

8
not_a_good_idea -> 

There are several things wrong with this procedure.
 - No matter what the parameter is, the procedure prints a 1. There is no need to set x = 1 to do that. In fact there is no need to call a procedure to print a 1 at all.
 - You shouldn't modify a parameter. If you need to use the parameter in some way that needs modification, make another variable and set it equal to the parameter. Like this:
def not_a_good_idea(x):
    y = x
    y += 5   # Change y, not the parameter x
    print(y)

not_a_good_idea2
- You should not modify a loop variable inside the loop, our outside the loop for that matter. In other words, do not modify loop variables. If you need to, set up another variable.

not_a_good_idea3
- After all of that work in the for loop all this procedure does is print out the parameter x. You don't need a procedure for that. What the author probably wanted was to print t. 
