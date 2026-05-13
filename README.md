# Implementation-of-Filters

## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br> Convert the image from BGR to RGB.
</br> 

### Step3
</br>Apply the required filters for the image separately. </br> 

### Step4
</br> Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>End the program.
</br> 

## Program: 
### Developed By   :VEDHANTH H 
### Register Number:212224240181
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python


import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Imgage2.jpg")
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
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
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
iv)Using Median Filter
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
i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
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
</br>

i) Using Averaging Filter
</br>
</br>
</br>
<img width="668" height="517" alt="image" src="https://github.com/user-attachments/assets/90582050-601c-4acc-b452-abdf76aa51bc" />

</br>
</br>

ii)Using Weighted Averaging Filter
</br>
</br>
</br>
<img width="960" height="768" alt="image" src="https://github.com/user-attachments/assets/d7ded729-6ca4-472c-992f-8b6b80db2778" />

</br>
</br>

iii)Using Gaussian Filter
</br>
</br>
<img width="654" height="516" alt="image" src="https://github.com/user-attachments/assets/d621083a-8e59-4de7-a3e3-3f06fde26daf" />

</br>
</br>
</br>

iv) Using Median Filter
</br>
</br>
</br>
</br>
<img width="961" height="764" alt="image" src="https://github.com/user-attachments/assets/5213c65e-2d66-4ec8-bab0-fb5934175f51" />

</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
</br>
<img width="652" height="508" alt="image" src="https://github.com/user-attachments/assets/1e8afde6-3ebc-4e0c-87c9-807a533abe46" />

</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
<img width="685" height="519" alt="image" src="https://github.com/user-attachments/assets/e35deb03-1daf-4027-9852-e5ad7e29447d" />

</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
