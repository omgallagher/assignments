# Lab-2d
## This is my assignment code
### 1. 
### a. Convert kg to lbs

```python
kg = float(input("Enter weight in kilograms: "))
pounds = kg*2.2
print(f"Weight in pounds: {pounds}")
```
### b. Calculate Credit Card Interest
```python
netBalance = float(input("Enter net balance: "))
payment = float(input("Enter payment amount: "))
d1 = int(input("Enter number of days in billing cycle: "))
d2 = int(input("Enter number of days before end of billing cycle payment was made: "))
interestratepermonth = float(input("Enter monthly interest rate (e.g., 0.0152 for 1.52%): 0.0152 "))

averageDailyBalance = (netBalance * d1 - payment * d2) / d1
interest = averageDailyBalance * interestratepermonth

print(f"Interest rate: {interest}")
```
### c. Distance between two cars
```python
x = float(input("Enter speed of Car A (west): "))
y = float(input("Enter speed of Car B (south): "))
t_hours = float(input("Enter elapsed time in hours: "))

distance = ((x * t_hours) ** 2 + (y * t_hours) ** 2) ** 0.5

hours = int(t_hours)
minutes = int((t_hours - hours) * 60)

print(f"Elapsed time: {hours} hours and {minutes} minutes")
print(f"Distance between cars: {distance}")
```

### 2.
'hello = "hello"'
Is a string, works fine
'_var = 100'
Works because it can start with an underscore
'1var = 200'
Doesn't work because it starts with a number
'print = "print me"'
Doesn't work because it's overwritten
'False = 0'
Doesn't work because false is a reserved and can't be reassigned
```
;Challanges I faced was creating the code to fit the commands I needed to conduct and making sure that they worked properly.
