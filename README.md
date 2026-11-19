# Exp 7-Lane Detection Using Hough Transform

##  Developed By

* **Name:** Srinivas J
* **Register No:** 212225230276

---

##  Aim

To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

---

## Learning Objective

* Understand each stage of image processing
* Learn how to build a complete computer vision pipeline
* Practice writing code in guided sections
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
image = cv2.imread('lane.webp')

if image is None:
    print("Image not found")
else:
    print("Image loaded successfully")

```

---

###  Step 3: Convert to Grayscale

```python

gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

```

---

###  Step 4: Display Images

```python
plt.figure(figsize=(10,5))
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()

```

---

###  Step 5: Thresholding

```python
threshold = cv2.threshold(gray, 150, 255, cv2.THRESH_BINARY)[1]
```

---

###  Step 6: Region of Interest (ROI)

```python
# ROI masking already provided
# (Do not modify)
```

### Step 7: Edge Detection (Canny)

```python
edges = cv2.Canny(gray, 50, 150)

```

---

###  Step 8: Gaussian Blur

```python

blur = cv2.GaussianBlur(edges, (5, 5), 0)

```

---

###  Step 9: Hough Transform

```python

lines = cv2.HoughLinesP(
    blur,
    1,
    np.pi / 180,
    50,
    minLineLength=50,
    maxLineGap=100
)

```

---

### Step 10: Lane Detection Logic

```python
# Already implemented
# (Do not modify)
```

---

##  Expected Output

* Original image
* Grayscale image
* Thresholded image
* ROI masked image
* Edge detected image
* Smoothed image
* Detected lines
* Final lane detection output

---
## Output

<img width="1589" height="779" alt="download" src="https://github.com/user-attachments/assets/8d5970fd-2c0a-4d13-95e4-712ddf8b29f0" />


---

## Result

Thus, the lane detection pipeline is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.

---
