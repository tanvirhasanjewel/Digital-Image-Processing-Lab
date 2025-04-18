# Digital Image Processing Lab
- **[Audity Ghosh](https://github.com/AudityGhosh)**
- **University of Information Technology and Sciences (UITS)**

## Image Processing Lab Tasks  

This repository contains Python implementations of fundamental image processing operations using OpenCV and NumPy. The tasks cover region extraction, color space conversion, geometric transformations, bitwise operations, and custom filtering.

---

## Task 1: Basic Image Operations  

### (a) Extracting a 100×100 Region from Image Center  
**Objective**: Crop a central 100×100 region from an image.  
**Code**:  
```python
import cv2
import numpy as np

# Load image from URL
image = cv2.imread('image.jpg')
h, w = image.shape[:2]
center_x, center_y = w // 2, h // 2

# Extract 100x100 region
cropped = image[center_y-50:center_y+50, center_x-50:center_x+50]

# Display
cv2.imshow('Original', image)
cv2.imshow('Cropped', cropped)
cv2.waitKey(0)
```

### (b) HSV Color Space Conversion  
**Objective**: Convert RGB to HSV and visualize components.  
**Code**:  
```python
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
hue, sat, val = cv2.split(hsv)

# Display components
cv2.imshow('Hue', hue)
cv2.imshow('Saturation', sat)
cv2.imshow('Value', val)
```

---

## Task 2: Image Transformations  

### (a)-(d) Resize, Rotate, Flip, and Display  
**Transformations Applied**:  
1. Resize to 256×256  
2. 180° clockwise rotation  
3. Vertical flip  

**Code**:  
```python
resized = cv2.resize(image, (256, 256))
rotated = cv2.rotate(image, cv2.ROTATE_180)
flipped = cv2.flip(image, 0)

# Plot in 2x2 grid
import matplotlib.pyplot as plt
plt.subplot(2, 2, 1), plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.subplot(2, 2, 2), plt.imshow(cv2.cvtColor(resized, cv2.COLOR_BGR2RGB))
plt.subplot(2, 2, 3), plt.imshow(cv2.cvtColor(rotated, cv2.COLOR_BGR2RGB))
plt.subplot(2, 2, 4), plt.imshow(cv2.cvtColor(flipped, cv2.COLOR_BGR2RGB))
plt.show()
```

---

## Task 3: Bitwise Operations on Shapes  

### (a)-(h) Rectangle, Circle, and Bitwise Operations  
**Key Operations**:  
```python
# Create black canvases
rect_img = np.zeros((400, 400, 3), dtype=np.uint8)
circle_img = np.zeros_like(rect_img)

# Draw shapes
cv2.rectangle(rect_img, (150, 150), (250, 250), (0, 255, 0), -1)  # Green rectangle
cv2.circle(circle_img, (200, 200), 50, (255, 0, 255), -1)         # Magenta circle

# Bitwise operations
bitwise_and = cv2.bitwise_and(rect_img, circle_img)
bitwise_or = cv2.bitwise_or(rect_img, circle_img)
bitwise_xor = cv2.bitwise_xor(rect_img, circle_img)
```

**Output**:  
- **AND**: Shows intersection (where both shapes overlap)  
- **OR**: Combines both shapes  
- **XOR**: Shows non-overlapping regions  

---

## Task 4: Custom Filter Application  

### Weighted Filter (Manual vs OpenCV)  
**Filter Kernel**:  
```
[1 1 1]  
[1 2 1]  
[1 1 1]  
```
**Code**:  
```python
kernel = np.array([[1, 1, 1], [1, 2, 1], [1, 1, 1]]) / 10  # Normalized

# Manual convolution
manual_filtered = cv2.filter2D(image, -1, kernel)

# Display comparison
plt.subplot(1, 3, 1), plt.imshow(image, cmap='gray')
plt.subplot(1, 3, 2), plt.imshow(manual_filtered, cmap='gray')
plt.subplot(1, 3, 3), plt.imshow(cv2.filter2D(image, -1, kernel), cmap='gray')
plt.show()
```

---

## Requirements  
- Python 3.x  
- OpenCV (`pip install opencv-python`)  
- NumPy (`pip install numpy`)  
- Matplotlib (`pip install matplotlib`)  

## Usage  
1. Clone the repository:  
   ```bash
   git clone https://github.com/tanvirhasanjewel/Digital-Image-Processing-Lab.git
   ```
2. Run individual scripts for each task (e.g., `python task1.py`).  

---

## Results  
Each task demonstrates core image processing techniques:  
- **Task 1**: Spatial and color space manipulation  
- **Task 2**: Geometric transformations  
- **Task 3**: Logical operations between images  
- **Task 4**: Custom filtering effects  
 

--- 

Developed as part of a computer vision lab course. Adjust file paths in the code as needed for your local setup.
 
