# Lab-3b
## This is my assignment code
### 1.

### a. 
```python
n0 = int(input("Enter a non-negative, non-zero integer: "))

steps = 0

while n0 != 1:
    if n0 % 2 == 0:
        n0 = n0 // 2
    else:
        n0 = 3 * n0 + 1
    print(n0)
    steps += 1

print("steps =", steps)
```
### b.
```python
### Infinite Loop
while True:
    print("This will run forever...")
### Fixed Infinite Loop
while True:
    text = input("Type 'exit' to stop: ")
    if text.lower() == "exit":
        print("Loop stopped.")
        break
    else:
        print("You typed:", text)
```
### c.
```python
num1 = int(input("Enter the first integer: "))
num2 = int(input("Enter the second integer: "))

print("Choose operation: +, -, *, /")
op = input("Enter operator: ")

if op == "+":
    result = num1 + num2
elif op == "-":
    result = num1 - num2
elif op == "*":
    result = num1 * num2
elif op == "/":
    if num2 == 0:
        result = "Error: Division by zero"
    else:
        result = num1 / num2
else:
    result = "Invalid operator"

print("Result:", result)

choice = input("Do you want to continue? (Y/N): ")
if choice.lower() != "y":
    print("Have a good day.")
```

### 2.
```python
text = input("Enter a sentence: ")

text = text.lower()

letter_counts = {}
total_letters = 0

for ch in text:

    if 'a' <= ch <= 'z':
        total_letters += 1
        if ch in letter_counts:
            letter_counts[ch] += 1
        else:
            letter_counts[ch] = 1
print("Total number of alphabets: ", total_letters)
print("Total number of distinct alphabets are:")

for letter in sorted(letter_counts.keys()):
    print(letter.upper(), "=", letter_counts[letter])
```
