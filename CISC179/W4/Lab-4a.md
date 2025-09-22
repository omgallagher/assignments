# Lab-4a
## This is my assignment code
### 1.
### a.
```python
my_tuple = tuple(input(f"Enter value {i+1}: ") for i in range(5))
print("Your tuple:", my_tuple)
```
### b.
; You would have to modify the new value to an element in a tuple by converting it to a list so it can change, and then turn it back to a tuple
```python
my_tuple = (9, 0)
temp_list = list(my_tuple)
temp_list[0] = 8
my_tuple = tuple(temp_list)
print(my_tuple)
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
; Values have their references stored in tuples and lists, so if the same value will appear more frequently then it may have the same memory address
; Challanges I faced was trying to understand how to use tuple correctly and working around the limits tuple has

