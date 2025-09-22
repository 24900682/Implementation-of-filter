# NAME: ASWIN.L
# REG NO: 212224230028 
# EXP-5 Implementation-of-filter
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
</br>

Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 

## Program:
### Developed By : ASWIN.L
### Register Number: 212224230028
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("me.jpg")
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
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()

```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.title("Median Blur")
plt.axis('off')
plt.show()

```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()

```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()

```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter

<img width="770" height="473" alt="Screenshot 2025-09-22 211009" src="https://github.com/user-attachments/assets/0c1c327a-888d-4d1c-b3f3-7aefd8033e3a" />

ii)Using Weighted Averaging Filter

<img width="340" height="431" alt="Screenshot 2025-09-22 211016" src="https://github.com/user-attachments/assets/dc6c6d6b-74c9-484c-8be5-49c6c66529ea" />

iii)Using Gaussian Filter

<img width="349" height="436" alt="Screenshot 2025-09-22 211021" src="https://github.com/user-attachments/assets/dc52dc95-07fc-408f-84cb-4f8a134dbf9e" />

iv) Using Median Filter
<img width="380" height="422" alt="Screenshot 2025-09-22 211028" src="https://github.com/user-attachments/assets/b5a32538-6241-4180-8af3-e0f96015b95d" />


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

<img width="363" height="442" alt="Screenshot 2025-09-22 211033" src="https://github.com/user-attachments/assets/fb077467-4c7d-4efa-af58-041bea8c41c3" />

ii) Using Laplacian Operator

<img width="340" height="429" alt="Screenshot 2025-09-22 211038" src="https://github.com/user-attachments/assets/61ce9513-c9cf-4d12-8679-7c4810352b61" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
