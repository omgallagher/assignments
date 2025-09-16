# Lab-3c
## This is my assignment code
### 1. 

### a.
```python
my_list = list(range(100))
print(type(my_list) is list)

my_list.append(100)
popped = my_list.pop()
my_list.reverse()
idx_50 = my_list.index(50)

print("popped:", popped)
print("idx_50:", idx_50)
print("first 10:", my_list[:10])
```
### b.
```python
lst = list(range(0, 10))
lst = lst[-3:] + lst[:-3]
print(lst)
```
### c.
```python
print(len([[1, 2]] * 3))
```
;Result would be 3
### d.
```python
my_list_ten_mem = [id(item) for item in my_list_ten]
print("IDs:", my_list_ten_mem)

from collections import defaultdict
positions = defaultdict(list)
for i, ident in enumerate(my_list_ten_mem):
    positions[ident].append(i)

print("Duplicate identities (id -> indices):")
for ident, idxs in positions.items():
    if len(idxs) > 1:
        print(hex(ident), "->", idxs)

print("Unique identities count:", sum(1 for idxs in positions.values() if len(idxs) == 1))
```
### e.
```python
del my_list_ten
```
### f.
```python
my_new_list_mem = [id(item) for item in my_new_list]

print("Old memory addresses:", my_list_ten_mem)
print("New memory addresses:", my_new_list_mem)

# Compare element by element
print("Same identities?:", [my_list_ten_mem[i] == my_new_list_mem[i] for i in range(10)])
```
### g.
```python
x = [[1, 2,3], [4, 5, 6], [7, 8, 9]]

y = [row[:] for row in x]
y[0][0] = 999
print("x:", x)
print("y:", y)

import copy
y2 = copy.deepcopy(x)
```
### h.
```python
pairs = [(i, i*i) for i in range(6)]
grid = [(i, j) for i in range(3) for j in range(3) if i != j]
labels = ["even" if i % 2 == 0 else "odd" for i in range(6)]
print(pairs, grid, labels, sep="\n")
```
### i.
```python
s = "To be, or not to be, this is the question"
spaces = len([ch for ch in s if ch == " "])
print("Number of spaces:", spaces)
```
### j.
```python
nums = [5, 2, 9]

nums.append(7)

nums.extend([8, 12])

nums.insert(1, 81)

nums.remove(7)

nums.sort()
print(nums)
```
;A challange I was having was trying to figure out the difference and significance of equality and idenity in python/ trying to know how to use them correctly.
