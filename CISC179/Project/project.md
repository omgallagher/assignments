# Project 1
## This is my assignment code
```python
from PIL import Image, ImageFilter
import os

image1 = Image.open('kitty.jpg')
image1.convert(mode='L').filter(ImageFilter.GaussianBlur(radius=2)).save('kittyafter.jpg')

image2 = Image.open('birdie.jpg')
image2.convert(mode='L').filter(ImageFilter.GaussianBlur(radius=2)).save('birdieafter.jpg')

os.makedirs("png", exist_ok=True)
for file in os.listdir('.'):
    if file.endswith('.jpg'):
        i = Image.open(file)
        file_name, file_ext = os.path.splitext(file)
        i.save(os.path.join("png", f"{file_name}.png"))

file = open("READ ME.txt", "w")
file.write("kittyafter.png, birdieafter.png")
file.close()
```
