# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the modules need to perform image filtering

### Step2
For performing smoothing operation of an image

Average filter
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)

Weighted average filter
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1

Gaussian Blur
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)

Median filter
median=cv2.medianBlur(image2,13)

### Step3

For performing sharpening on a image.

Laplacian Kernel
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)

Laplacian Operator
laplacian=cv2.Laplacian(image2,cv2.CV_64F)

### Step4

Display all the images based on the filter type

### Step5

End the program

## Program:
### Developed By   :Shakthi kumar S
### Register Number:212222110043

import cv2
import matplotlib.pyplot as plt
import numpy as np
1=cv2.imread("sk.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
plt.imshow(image1)
plt.axis("off")
plt.show()
plt.imshow(image2)
plt.axis("off")
plt.show()

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()

```
ii) Using Weighted Averaging Filter

```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter

```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

iv) Using Median Filter

```Python
dian=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Kernal

```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator

```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter
![DIP06-1](https://user-images.githubusercontent.com/121041644/230023927-43f89468-1013-438e-bd74-d49083f4aa30.png)

ii) Using Weighted Averaging Filter
![DIP06-2](https://user-images.githubusercontent.com/121041644/230024067-cddf7c0d-eb52-482a-9bb9-54f6cee8f9f3.png)

iii) Using Gaussian Filter
![DIP06-3](https://user-images.githubusercontent.com/121041644/230024282-3a511aed-d57f-47ec-9d79-3837b61385b5.png)

iv) Using Median Filter
![DIP06-4](https://user-images.githubusercontent.com/121041644/230024395-1ff19503-26d5-4e65-b08b-1261b891438e.png)

### 2. Sharpening Filters

i) Using Laplacian Kernal
![DIP06-5](https://user-images.githubusercontent.com/121041644/230024514-40e62253-924c-4ce6-801b-52f07b51448c.png)

ii)Using Laplacian Operator
![DIP06-6](https://user-images.githubusercontent.com/121041644/230024559-92b89603-90bf-48c4-bcf7-7cd37c581e1d.png)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
