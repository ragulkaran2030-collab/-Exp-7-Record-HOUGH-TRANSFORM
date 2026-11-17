# Exp-7 Lane Detection

##  Developed By

* **Name:** KARANKUMAR K
* **Register No:** 212225040171

##  Aim

To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

---

## Learning Objective

* Understand each stage of image processing
* Learn how to build a complete computer vision pipeline
* Practice writing code in guided sections

**Important Instruction:**
👉 Write code **ONLY in places marked as `# Your Code Here`**
👉 Do NOT modify any other part of the code

---

##  Software Used

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

---

##  Algorithm & Explanation

---

###  Step 1: Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

---

###  Step 2: Read the Image

```python
# Read the image

###
image = cv2.imread('lan.webp')

if image is None:
    print("Image not found")
else:
    print("Image loaded successfully")

###
```

---

###  Step 3: Convert to Grayscale

```python
# Convert to grayscale.

###

gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

###
```

---

###  Step 4: Display Images

```python
plt.figure(figsize=(10,5))

###
plt.figure(figsize=(10,5))
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()

###
```

---

###  Step 5: Thresholding

```python
# Apply thresholding

threshold = 
###
threshold = cv2.threshold(gray, 150, 255, cv2.THRESH_BINARY)[1]

###
```

---

###  Step 6: Region of Interest (ROI)

```python
# ROI masking already provided
# (Do not modify)

```

---

### Step 7: Edge Detection (Canny)

```python
# Perform Edge Detection

###
edges = cv2.Canny(gray, 50, 150)

###
```

---

###  Step 8: Gaussian Blur

```python
# Apply Gaussian Blur

###

blur = cv2.GaussianBlur(edges, (5, 5), 0)

###
```

---

###  Step 9: Hough Transform

```python
# Detect lines using Hough Transform

###

lines = cv2.HoughLinesP(
    blur,
    1,
    np.pi / 180,
    50,
    minLineLength=50,
    maxLineGap=100
)

###
```

---

### Step 10: Lane Detection Logic

```python
# Already implemented
# (Do not modify)
```

---

##  Expected Output

<img width="1589" height="744" alt="download" src="https://github.com/user-attachments/assets/583cf5fa-68c1-4f19-9f27-ea6727368d2c" />


* Original image
* Grayscale image
* Thresholded image
* ROI masked image
* Edge detected image
* Smoothed image
* Detected lines
* Final lane detection output

---

##  Instructions

* Fill ONLY in `# Your Code Here` sections
* Do NOT change existing code
* Run step-by-step
* Verify outputs

---

## Result

Thus, the lane detection pipeline is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.

---


