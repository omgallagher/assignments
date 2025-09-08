# Lab-2c
## Assignment code 
### Variable memory usage

```python
var1 = 10
print(hex(id(var1)))

var1 = 100
print(hex(id(var1)))
```
;There are two different adresses because of how the integers are immutable and what happened to the first one was that a new object in memory was created. 

```python
var2 = 100
print(hex(id(var2)))
```
;Python resued the same memory address as var1 because python uses integer interning

# Memory map
```python
str1 = "Hello"
str2 = "World"

| Address in hexadecimal | Char |
| ---------------------- | ---- |
| #0x7ffc416f6b30        |  H   |
| #0x7ffc416f70a0        |  E   |
| #0x7ffc416f71f0        |  L   |
| #0x7ffc416f71f0        |  L   |
| #0x7ffc416f7280        |  O   |
| #0x7ffc416f6e00        |  W   |
| #0x7ffc416f7280        |  O   |
| #0x7ffc416f7310        |  R   |
| #0x7ffc416f71f0        |  L   |
| #0x7ffc416f7070        |  D   |
```

# Problem solving
```python
x = "dog"
y = "cat"
x + y = "dogcat"
"the" + x + "chases the" + y = "the dog chases the cat"
x*4 = "dogdogdogdog"
x = 50
x = x + 1
print(x)
;Output is 51
```

# Troubleshooting
```python
hello = "hello"
;Doesn't work because of how keywords can't be variables
_var = 100
;Works
!var_1 = 200
;Doesn't work since a variable can't start with that
print = "print me"
;Doesn't work since it overides 'print'
False = 0
;Doesn't work because keywords can't be assigned
```

;Challanges I faced was remembering why some variable names is and isn't invalid, it's easy to get the rules mixed up with each other.
