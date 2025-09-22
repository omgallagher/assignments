# Lab-4c
## This is my assignment code
### 1.
### a.
```python
def convert_kpl_to_mpg(kpl):
    return round(kpl * 0.42514, 2)
def convert_mpg_to_kpl(mpg):
    return round(mpg * 0.42514, 2)
def main():
    print("Welcome to Unit Converter")
    print("Choose conversion direction:")
    print("1. kpl to mpg")
    print("2. mpg to kpl")
    choice = input("Enter 1 or 2:")
    if choice not in ["1", "2"]:
        print("Invalid choice.")
        return
    values = input("Enter values seperated by commas: ")

    try:
        numbers = [float(v.strip()) for v in values.split(",")]
    except ValueError:
        print("Please enter only numeric values.")
        return
    if choice == "1":
      for kpl in numbers:
          print(f"{kpl} kpl = {convert_kpl_to_mpg(kpl)} mpg")
    else:
        for mpg in numbers:
            print(f"{mpg} mpg = {convert_mpg_to_kpl(mpg)} kpl")
main()
```
### b.
```python
def reverse_print(*args):
    for val in reversed(args):
        print(val)
reverse_print("apple", "cherry", "banana")
```
### c.
; What would result from changing a list or dictionary is that whatever changes were made inside of the function, they will affect the outside of it.
```python
def modify_list(my_list):
    my_list.append(99)
def modify_dict(my_dict):
    my_dict["new_key"] = "new_value"
l = [1, 2, 3]
d = {"a": 1}
modify_list(l)
modify_dict(d)
print("Modified list:", l)
print("Modified dict:", d)
```
### Minimize the risk
```python
def safe_modify_list(my_list):
    my_list = my_list.copy()
    my_list.append(999)
safe_modify_list(l)
print("Safely unchanged list:", l)
```
### d.
```python
x = 5
def funct_1():
    x = 3
    
def funct_2():
    x = 2
funct_1()
print("After funct_1, x =", x)
funct_2()
print("After funct_2, x =", x)
```
; The value of x after computing both functions will be 5

### 2.
### a.
```python
def my_func(a, b, numbers):
    print("a =", a)
    print("b =", b)
    print("numbers =", numbers)

my_func(1, 2, [3, 4, 5, 6])
```
; Option 3 works because it's possible to group numbers into a single object to create one argument
### b.
```python
def my_func_global():
  x = 100

global x
x = 10
my_func_global()
print(x)
```
; This code prints out x = 10 because the global keyword was placed incorrectly
```python
def my_func_global():
    global x
    x = 100

x = 10
my_func_global()
print(x)
```
; The global keyword is placed in the correct spot in order to get x = 100

; Challanges I experienced was trying to fix the error for 'my_func' because it the way I wrote it, it kept coming up as error so it was tricky to find something that could work.
