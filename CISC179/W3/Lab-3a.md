# Lab-3a
## This is my assignment code
### 1.
```python
for code in range(32, 127):
    ch = chr(code)
    label = 'SP' if ch == ' ' else ch
    print(f"{code:>3} : {label}")
```

### 2.
```python
print(10 > 4 and 50 < 100)
print(10 < 4 and 50 < 100)
print(10 < 4 and 50 > 100)
print(10 > 4 and 50 > 100)
print(not (10 > 4))
```

### 3.
```python
x = 0b1110
y = 0b1011
result = x | y
print(result)
print(bin(result))
```

### 4.
```python
number1 = int(input("Enter the first number: "))
number2 = int(input("Enter the second number: "))
if number1 > number2:
    larger_number = number1
else:
    larger_number = number2
print("The larger number is:", larger_number)

x = 10
if x > 5:
    if x == 6:
        print("nested x == 6")
    elif x == 10:
        print("nested x == 10")
    else:
        print("nested: else")
else:
    print("else")
```

### 5.
### a.
```python
a = int(input("Enter a: "))
b = int(input("Enter b: "))
c = int(input("Enter c: "))
largest = a
if b > largest:
    largest = b
if c > largest:
    largest = c
print("Largest is:", largest)
```
### b.
```python
n = int(input("Enter an integer: "))
print("Approach 1:", "even" if n % 2 == 0 else "odd")
print("Approach 2:", "even" if (n & 1) == 0 else "odd")
print("Approach 3:", "even" if (n // 2) * 2 == n else "odd")
print("Approach 4:", "even" if (n & ~1) == n else "odd")
```
### c.
```python
pct = int(input("Enter your percentage (integer): "))
if pct < 0:
    print("Percentage cannot be negative.")
elif pct > 100:
    print("Percentage cannot exceed 100.")
else:
    if pct > 90:
        grade, desc = "A", "Work of genuinely superior quality"
    elif 80 <= pct <= 89:
        grade, desc = "B", "Passing performance falls approximately in the upper distribution of passing grades."
    elif 71 <= pct <= 79:
        grade, desc = "C", "Passing performance falls approximately in the center of the distribution of the distribution of all passing grades."
    elif 65 <= pct <= 70:
        grade, desc = "D", "Passing performance falls approximately in the lower distribution of passing grades."
    else:
        grade, desc = "F", "Failing performance that does not satisfy the basic requirements of the course and needs to be improved in significant ways."
print(f"Grade: {grade}\nDescription: {desc}")
```
### d.
```python
op = input("Enter a logical operator (and/or/not): ").strip().lower()

if op == "not":
    print("A | not A")
    print("--+------")
    for A in (False, True):
        print(f"{A!s:<5}{(not A)}")
elif op in ("and", "or"):
    print("A     B | A", op, "B")
    print("-----------+---------")
    for A in (False, True):
        for B in (False, True):
            if op == "and":
                result = A and B
            else:
                result = A or B
            print(f"{A!s:<5} {B!s:<5} | {result}")
else:
    print("Unsupported operator. Please enter and/or/not.")
```
### e.
```python
n = int(input("Enter an integer: "))
if n & 1:
    print("odd")
else:
    print("even")
```

### 6.
```python
name = input("What's your name? ")
time = int(input("What time is it?"))
if 0 <= time <= 1159:
    print("Hi " + name + ", good morning!")
elif 1200 <= time <= 1759:
    print("Hi " + name + ", good afternoon!")
else:
    print("Hi " + name + ", good evening!")
print("Good Bye")
```

### 7.
```python
x = 1
y = 1.0
z = "1"

if x == y:
    print("one")
if y == int(z):
    print("two")
elif x == y:
    print("three")
else:
    print("four")
;The output for this is code two
```
;Some challanges I had with this practice lab was making sure I knew the difference between bitwise and logical operators and figuring out when I should incorperate them.
