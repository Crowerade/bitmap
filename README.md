# bitmap
Write bitmap files (.bmp) in pure Python.

This is a very simple script to write .bmp files. You can easily drop it in a repository and use it for your project.

## Usage
The following code sample shows the full interface of the Bitmap class.
```Python
from bitmap import Bitmap

# Create a bitmap 10px by 10px with a grey background.
bmp = Bitmap(10, 10, fill=(51, 51, 51))

# Draw a diagonal blue line.
for i in range(8):
    bmp.pencil(i + 1, i + 1, (0, 100, 255))
    
# Save the file.
bmp.save('diag_blue_line.bmp')
```

## Notes
A few simple things to keep in mind:
1. The origin of the drawing (0, 0) is in the top-left corner.
2. Colors should be provided as (R, G, B) tuples.
3. The file is written in 24-bit color, so each color value can range from 0-255.
