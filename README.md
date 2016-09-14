1 s = "23" + "!@" + "alm". What is the value of s?

2 s = s + "3". Is this a proper one line program?

3
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

4 What is the output of the following program?
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

5 What is the output of the following programs?
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

6 What is the output of the following programs?
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
