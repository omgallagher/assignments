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
