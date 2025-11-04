# EX 6: EDGE-DETECTION
# NAME : Markandeyan Gokul
# REG NO : 212224240086
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
Name : Markandeyan Gokul
Reg no : 212224240086
```

## ORIGINAL IMAGE:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('puppy.png')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## SOBEL EDGE DETECTOR:
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## LAPLACIAN EDGE DETECTOR:
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
## CANNY EDGE DETECTOR:
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```

## Output:
## ORIGINAL IMAGE
<img width="641" height="472" alt="Screenshot 2025-10-10 210540" src="https://github.com/user-attachments/assets/f967e8b7-1c5d-4e53-8e16-23ce0d6dd955" />

## SOBEL EDGE DETECTOR:
<img width="649" height="467" alt="Screenshot 2025-10-10 210656" src="https://github.com/user-attachments/assets/24050a2b-a48a-4bf0-9bf9-f7f5ea87ac68" />

## LAPLACIAN EDGE DETECTOR:
<img width="653" height="480" alt="Screenshot 2025-10-10 210628" src="https://github.com/user-attachments/assets/f2dc123d-15bb-47ed-81a8-49d9a341188d" />

## CANNY EDGE DETECTOR:
<img width="673" height="480" alt="Screenshot 2025-10-10 210641" src="https://github.com/user-attachments/assets/2270d135-2bc7-4120-abe1-a1bc0f42eb1c" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
