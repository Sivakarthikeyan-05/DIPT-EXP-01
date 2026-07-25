
# EXPERIMENT 1 - IMAGE HANDLING AND PIXEL TRANSFORMATIONS USING OPENCV

## Name
**Sivakarthikeyan V**

## Register Number
**212225220098**

---

# Step 1: Read and Display the Image

```python
import cv2
import matplotlib.pyplot as plt

# Read the image using OpenCV
img = cv2.imread('1.jpg', cv2.IMREAD_COLOR)

# Convert BGR to RGB
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

# Display the image
plt.imshow(img_rgb)
plt.title("Original Image")
plt.axis('off')
plt.show()
```

<img width="646" height="399" alt="image" src="https://github.com/user-attachments/assets/09741374-7261-4c71-be81-0580c60b6dbb" />

---

# Step 2: Drawing Operations

## Draw a line from the top-left to the bottom-right of the image

```python
# Load the image
image = cv2.imread('1.jpg')

# Convert BGR to RGB
img_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Draw a line
line_img = cv2.line(img_rgb.copy(), (0, 0), (799, 599), (255, 0, 0), 10)

plt.imshow(line_img)
plt.title("Image with Line")
plt.axis('off')
plt.show()
```

<img width="642" height="391" alt="image" src="https://github.com/user-attachments/assets/ab2cee59-ef72-4ca3-a2de-f4ddba269ac0" />

---

## Draw a circle at the center of the image

```python
# Load the image
image = cv2.imread('1.jpg')

# Convert BGR to RGB
img_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Draw a circle
circle_img = cv2.circle(img_rgb.copy(), (400, 300), 150, (255, 0, 0), 10)

plt.imshow(circle_img)
plt.title("Image with Circle")
plt.axis('off')
plt.show()
```

<img width="640" height="398" alt="image" src="https://github.com/user-attachments/assets/61840d84-ac21-42b3-bf06-a17e5841a13c" />

---

## Draw a rectangle around the whole image

```python
# Load the image
image = cv2.imread('1.jpg')

# Convert BGR to RGB
img_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Draw rectangle
rectangle_img = cv2.rectangle(img_rgb.copy(), (0, 0), (799, 599), (255, 0, 255), 10)

plt.imshow(rectangle_img)
plt.title("Image with Rectangle")
plt.axis('off')
plt.show()
```

<img width="643" height="391" alt="image" src="https://github.com/user-attachments/assets/8c7f3b62-86ba-4577-a839-b853d2a22950" />

---

## Add text at the top-left corner of the image

```python
# Load the image
image = cv2.imread('1.jpg')

# Convert BGR to RGB
img_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Add text
text_img = cv2.putText(
    img_rgb.copy(),
    "OpenCV Drawing",
    (20, 40),
    cv2.FONT_HERSHEY_SIMPLEX,
    1,
    (255, 255, 0),
    2
)

plt.imshow(text_img)
plt.title("Image with Text")
plt.axis('off')
plt.show()
```

<img width="644" height="398" alt="image" src="https://github.com/user-attachments/assets/cef00052-ffbe-4ebc-8214-3435c8cd16c0" />

---

# Step 3: Color Space Conversions

## Convert RGB to HSV

```python
image = cv2.imread('1.jpg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)

plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
plt.show()
```

<img width="642" height="405" alt="image" src="https://github.com/user-attachments/assets/c120c8cc-03fd-4af1-9aef-3769e2f2b564" />

---

## Convert RGB to Grayscale

```python
image = cv2.imread('1.jpg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)

plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
plt.show()
```

<img width="642" height="399" alt="image" src="https://github.com/user-attachments/assets/2f8df240-5c3d-4a79-acf0-d84280498086" />

---

## Convert RGB to YCrCb

```python
image = cv2.imread('1.jpg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)

plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
plt.show()
```

<img width="640" height="398" alt="image" src="https://github.com/user-attachments/assets/fc03bb70-b375-434f-abce-e275f37537de" />

---

## Convert HSV back to RGB

```python
image = cv2.imread('1.jpg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)

plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
plt.show()
```

<img width="639" height="395" alt="image" src="https://github.com/user-attachments/assets/45b7f970-1f26-4bd6-b993-465fb14c3708" />

---

# Step 4: Pixel Access and Modification

## Access and print the pixel value at (100,100)

```python
image = cv2.imread('1.jpg')

print("Pixel Value at (100,100):", image[100,100])
```

---

## Modify the pixel at (200,200) to white

```python
image = cv2.imread('1.jpg')

image[200,200] = [255,255,255]

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.title("Modified Pixel")
plt.axis("off")
plt.show()
```

---

## Modify a 300×300 block of pixels to white

```python
image = cv2.imread('1.jpg')

image[200:500,200:500] = [255,255,255]

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.title("Image with White Block")
plt.axis("off")
plt.show()
```

<img width="649" height="402" alt="image" src="https://github.com/user-attachments/assets/49c60abc-12e3-431f-97ca-51c74ea2cb7c" />

---

# Step 5: Resize the Image

## Resize the original image to half its size

```python
image = cv2.imread('1.jpg')

resized_image = cv2.resize(image, (400,300))

resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)

plt.imshow(resized_image_rgb)
plt.title("Resized Image")
plt.axis("off")
plt.show()
```
<img width="611" height="508" alt="image" src="https://github.com/user-attachments/assets/2e5b13fd-bf82-420b-b712-26ae23709c2a" />
---

# Step 6: Crop the Region of Interest (ROI)

## Crop a region of interest from the image

```python
image = cv2.imread('1.jpg')

roi = image[50:350,50:350]

roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)

plt.imshow(roi_rgb)
plt.title("Cropped ROI")
plt.axis("off")
plt.show()
```

<img width="487" height="506" alt="image" src="https://github.com/user-attachments/assets/16b03a70-32d4-494b-9c52-d955ef715af3" />


---

# Step 7: Flip the Image

## Flip the image horizontally

```python
image = cv2.imread('1.jpg')

flipped_horizontally = cv2.flip(image,1)

flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)

plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
plt.show()
```

<img width="638" height="393" alt="image" src="https://github.com/user-attachments/assets/4d8d6275-3eb3-4ab5-b48c-ef2f0d03e713" />

---

## Flip the image vertically

```python
image = cv2.imread('1.jpg')

flipped_vertically = cv2.flip(image,0)

flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)

plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
plt.show()
```

<img width="642" height="394" alt="image" src="https://github.com/user-attachments/assets/dc7570d1-0c77-4f0b-b038-3c2afeb879e4" />

---

# Step 8: Save the Final Modified Image

## Save the final modified image to the local directory

```python
image = cv2.imread('1.jpg')

cv2.imwrite("final_modified_image.jpg", image)

print("Image saved successfully!")
```
