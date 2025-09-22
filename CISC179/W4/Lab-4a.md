# Lab-4a
## This is my assignment code
### 1.
### a.
```python
my_tuple = tuple(input(f"Enter value {i+1}: ") for i in range(5))
print("Your tuple:", my_tuple)
```
### b.
```python
```
### c.
```python
from collections import Counter
my_tuple = (1, 2, 3, 4, 3, 2, 1, 2, 3, 5, 4, 3, 2, 1)
counter = Counter(my_tuple)
print("Count of each element:")
for item, count in counter.items():
    if count > 1:
        print(f"{item} appears {count} times")
```
### d.
```python
original_tuple = (1, 2, 3, 4, 3, 2, 1, 2, 3, 5, 4, 3, 2, 1)
new_tuple = original_tuple + original_tuple
print("original tuple ID:", id(original_tuple))
print("new tuple ID:", id(new_tuple))
```
### e.
x = (1,2,3,4)
x.append(1)
x[1] = "hello"
del x[2]
; The following doesn't work in tuples 
### 2.
### a.
```python
(one, two, three, four) = (1, 2, 3, 4)
print(type(one))
print(type(two))
print(type(three))
print(type(four))
```
### b.
```python
x = (1, 2, 3, 4)
a, b, *c = x
print(a, b, c)
```
### c.
```python
x = (1, 2, 3, 4)
a, b, *c = x
print(a)
print(b)
print(c)
```
; The result is 1, 2, [3, 4]
### 3.
```python
my_x = [100, 200, 300, 400]
my_y = (200, 300, 400, 500)
for i in range(len(my_x)):
    print(f"Index {i} - my_x: {id(my_x[i])}, my_y: {id(my_y[i])}")
```
; Index 0 - my_x: 140721206886408, my_y: 140721206889608
; Index 1 - my_x: 140721206889608, my_y: 1626351966704
; Index 2 - my_x: 1626351966704, my_y: 1626355194032
; Index 3 - my_x: 1626355194032, my_y: 1626355194224
