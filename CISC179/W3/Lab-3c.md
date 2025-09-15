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
