---
date: 2024-03-16
tags:
    - code-snip
hubs:
    - "[[python]]"
---

# Convert clip art image png to color

Replaces all non-zero colors in image with a single color
```python
from PIL import Image


INPUT_PATH = (
    "/Users/alex/Temp/faceless-creepypasta/assets/drawn-yellow-circle-clipart-xl.png"
)
OUTPUT_PATH = (
    "/Users/alex/Temp/faceless-creepypasta/assets/drawn-red-circle-clipart-xl.png"
)


def convert_image_to_red(input_path, output_path):
    # Load the image
    image = Image.open(input_path).convert("RGBA")
    width, height = image.size

    # Prepare the red color with the desired hex code, including a dummy alpha
    red_color = (230, 0, 0)  # This corresponds to #e60000

    # Process every pixel
    for x in range(width):
        for y in range(height):
            r, g, b, alpha = image.getpixel((x, y))
            # If the pixel is not fully transparent, change its color to red while preserving its alpha value
            if alpha != 0:
                image.putpixel((x, y), red_color + (alpha,))

    # Save the modified image
    image.save(output_path)


convert_image_to_red(INPUT_PATH, OUTPUT_PATH)
print("Conversion complete. The output image is saved at:", OUTPUT_PATH)

```
