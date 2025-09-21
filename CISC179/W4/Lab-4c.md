### This is my assignment code

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
