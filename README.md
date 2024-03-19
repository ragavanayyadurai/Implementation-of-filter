# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.


### Step2
Convert the image from BGR to RGB.


### Step3
Apply the required filters for the image separately.


### Step4
Plot the original and filtered image by using matplotlib.pyplot.


### Step5
End the program.


## Program:
### Developed By   : Ragavendran A
### Register Number: 212222230114
### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("eiffle.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
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
plt.figure(figsize=(9,9))
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
plt.figure(figsize=(9,9))
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

median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()



```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
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
plt.figure(figsize=(9,9))
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

![Screenshot 2024-03-19 210842](https://github.com/ragavanayyadurai/Implementation-of-filter/assets/118749557/0fb6cffa-5bea-4c4f-8afb-edd1370afba3)

ii) Using Weighted Averaging Filter

![Screenshot 2024-03-19 211203](https://github.com/ragavanayyadurai/Implementation-of-filter/assets/118749557/9b1d611e-856a-46a2-bc38-7f36b4df0d46)

iii) Using Gaussian Filter

![Screenshot 2024-03-19 211254](https://github.com/ragavanayyadurai/Implementation-of-filter/assets/118749557/f2a5756b-58e6-49c2-b7a3-774d74f39463)

iv) Using Median Filter

![Screenshot 2024-03-19 211334](https://github.com/ragavanayyadurai/Implementation-of-filter/assets/118749557/dce33fc4-6e5e-4986-8250-c8d69d85384a)


### 2. Sharpening Filters

i) Using Laplacian Kernal

![Screenshot 2024-03-19 211358](https://github.com/ragavanayyadurai/Implementation-of-filter/assets/118749557/68f6e75f-adb5-4244-8f1d-806c59fa2468)

ii) Using Laplacian Operator

![Screenshot 2024-03-19 211523](https://github.com/ragavanayyadurai/Implementation-of-filter/assets/118749557/60b8a510-cd06-440c-ad5b-bdc1cef4007e)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
