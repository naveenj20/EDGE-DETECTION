# EDGE-DETECTION

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
image = cv2.imread('pandas.jpg')  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```


### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output:

### ORIGINAL IMAGE

![Screenshot 2025-04-23 212411](https://github.com/user-attachments/assets/3d3565e8-ce88-4b39-a770-2a465f4c290b)

### SOBEL EDGE DETECTOR

![Screenshot 2025-04-23 212430](https://github.com/user-attachments/assets/b8576907-6e35-4c7d-a090-f697608a5c81)

### LAPLACIAN EDGE DETECTOR

![Screenshot 2025-04-23 212447](https://github.com/user-attachments/assets/5879df84-a55f-47e7-8f4b-72e90d6604cc)

### CANNY EDGE DETECTOR

![Screenshot 2025-04-23 212506](https://github.com/user-attachments/assets/fae557c6-04a3-47f8-9f44-14eb37fe6faa)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
