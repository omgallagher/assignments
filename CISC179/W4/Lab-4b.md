# Lab-4b
## This is my assignment code
### 1.
### a.
```python
my_dict = {
    "name": "Olivia Gallagher",
    "gender": "Female",
    "age": "19",
    "date of birth": "September 2nd 2006",
    "address": "1797 Monarch Ridge Circle",
    "zip code": "92019",
    "city": "San Diego",
    "state": "California",
    "country": "United States",
    "email address": "ogallagher@student.sdccd.edu",
}
print(my_dict)
```
### b.
```python
my_user_dict = {}
while True:
    key = input("Enter field (e.g., SSN, Name): ")
    value = input(f"Enter value for {key}: ")
    my_user_dict[key] = value
    cont = input("Do you want to continue (y/n)? ")
    if cont.lower() != 'y':
        break
print("User Dictionary:", my_user_dict)
```
### c.
```python
data = [
    ('Name', 'Sarah Connor'),
    ('Date of Birth', '1 Jan 1980'),
    ('Address', '1000 Black Mountain Drive'),
    ('Zip', '92126'),
    ('Name', 'Jim Hawkins')
]
my_dict = {}
for pair in data:
    key = pair[0]
    value = pair[1]
while key in my_dict:
    print(f"Duplicate key '{key}' found. Please enter a new key.")
    key = input("New key: ")
    my_dict[key] = value
print("Validated Dictionary:", my_dict)
```
### d.
```python
```
### e. 
```python
text = """
The tiger (Panthera tigris) is a large cat and a member of the genus Panthera native to Asia. 
It has a powerful, muscular body with a large head and paws, a long tail and orange fur with black, mostly vertical stripes. 
It is traditionally classified into nine recent subspecies, though some recognise only two subspecies, mainland Asian tigers and the island tigers of the Sunda Islands.
"""
word_count = {}
words = text.replace("(", "").replace(".", "").lower().split()
for word in words:
    word_count[word] = word_count.get(word, 0) + 1
print(f"Occurences of 'the': {word_count.get('the', 0) + word_count.get('the', 0)}")
print("Total word frequencies:", word_count)
```
; Number of words is 66
### 2.
### a.
```python
d_orig = {123: "Coconut"}
d_copy = d_orig.copy()
d_copy[123] = "Mango"

print("Original:", d_orig)
print("Copy:", d_copy)
```
### b.
```python
```
### c.
```python
bad_dict = {[1, 2, 3]: "Invalid"}
```
; Using a mutable type like dict wouldn't work as a dictionary key because of how their hash value can change
