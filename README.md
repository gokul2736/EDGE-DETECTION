# EDGE-DETECTION
# Name: Markandeyan Gokul
# Reg: 212224240086
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Tiger.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
<img width="524" height="527" alt="image" src="https://github.com/user-attachments/assets/61b0beca-6f2b-4220-a7c0-5c01d2908f7b" />

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="1121" height="551" alt="image" src="https://github.com/user-attachments/assets/f58adfa8-20f2-4b3a-9ee4-a31e5d7e04ba" />

<img width="1160" height="555" alt="image" src="https://github.com/user-attachments/assets/7caae179-a819-488c-af59-4c7a6115e08f" />

<img width="1139" height="562" alt="image" src="https://github.com/user-attachments/assets/1a42c1ca-2ac1-4183-aaf7-e09b16782efc" />

### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

<img width="1113" height="556" alt="image" src="https://github.com/user-attachments/assets/6bfdc00f-bb04-4172-a22f-5c1721c65bb6" />

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
<img width="1171" height="567" alt="image" src="https://github.com/user-attachments/assets/e0d90f02-5666-4e99-bf2e-960ed6981d42" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
