# Dipt-exp-7
# Record-HOUGH TRANSFORM
##  Developed By
## Name: Nara Guna Susmitha
## Register No: 212224230176

##  Aim

To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

---

##  Software Used

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

---

##  Algorithm 

---
Step 1: Import Libraries

Step 2: Read the Image

Step 3: Convert to Grayscale

Step 4: Display Images

Step 5: Thresholding

Step 6: Region of Interest (ROI)

Step 7: Edge Detection (Canny)

Step 8: Gaussian Blur

Step 9: Hough Transform

Step 10: Lane Detection Logic


---

## Program
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('Qno. 1.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert image to RGB for displaying
plt.title("Input Image")
plt.axis('off')

plt.imshow(gray_image, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')

edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')

lines = cv2.HoughLinesP(edges, 1, np.pi / 180, 100, minLineLength=50, maxLineGap=10)
for line in lines:
    x1, y1, x2, y2 = line 
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Image with lines drawn
plt.title("Result of Hough Transform")
plt.axis('off')
```


## Output

<img width="395" height="452" alt="image" src="https://github.com/user-attachments/assets/17d68acc-0e9a-47eb-836d-a7859cc8bd7c" />

<img width="383" height="447" alt="image" src="https://github.com/user-attachments/assets/738756df-84ce-4bf6-9240-ac4e1c201a45" />

<img width="387" height="442" alt="image" src="https://github.com/user-attachments/assets/1a38924e-f9e6-4533-bef7-ac9b7a1fa3ce" />

<img width="386" height="442" alt="image" src="https://github.com/user-attachments/assets/d6c33bd7-c43d-4c34-9b33-2f8f57b0b9e6" />

---



## Result

Thus, the lane detection pipeline is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.

---

