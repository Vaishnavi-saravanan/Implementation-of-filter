![313991445-071a94f7-1c98-4cc5-aa51-da1084d64274](https://github.com/Vaishnavi-saravanan/Implementation-of-filter/assets/118541897/2b896d96-175f-455b-b8ea-1a5cca46dd00)# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries
### Step2
Convert the image from BGR to RGB.
### Step3
Apply the required filters for the image separately.
### Step4
Plot the original and filtered image by using matplotlib.pyplot.
### Step5
End the program.
## Program:
```
Developed By   : VAISHNAVI S
Register Number: 212222230165
```


### 1. Smoothing Filters

i) Using Averaging Filter
```

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("nebula.jpg")
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
```
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
```

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
```

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
```
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
```


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
![313991445-071a94f7-1c98-4cc5-aa51-da1084d64274](https://github.com/Vaishnavi-saravanan/Implementation-of-filter/assets/118541897/330176b4-1edc-44a1-ad28-9574c7c0d8f6)
ii) Using Weighted Averaging Filter
![313991488-4ebdd6e6-e027-41da-a476-6ddf2cf3d51f](https://github.com/Vaishnavi-saravanan/Implementation-of-filter/assets/118541897/8ebd704c-0a2d-4df1-8da0-90179b642d7d)
iii) Using Gaussian Filter
![313991523-59b7b210-b6d9-4631-9991-94c2c99e090b](https://github.com/Vaishnavi-saravanan/Implementation-of-filter/assets/118541897/cc8cc40f-760c-4ede-a846-1601c0c7acb7)
iv) Using Median Filter
![313991549-96f13828-7803-4313-ba03-a813f355ef9a](https://github.com/Vaishnavi-saravanan/Implementation-of-filter/assets/118541897/962e17bf-31d6-4edd-aae5-d40a0b1fe823)

### 2. Sharpening Filters

i) Using Laplacian Kernal
![313991601-a148ef5c-5076-4c92-bf00-33f3dbece1d0](https://github.com/Vaishnavi-saravanan/Implementation-of-filter/assets/118541897/9e1a386f-a577-45b2-9987-a0e84f52658d)

ii) Using Laplacian Operator

![313991834-0b40c602-759c-4d7e-a010-e687067ec4af](https://github.com/Vaishnavi-saravanan/Implementation-of-filter/assets/118541897/3d2cc345-eec7-4f02-bb46-29896c90a8b3)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
