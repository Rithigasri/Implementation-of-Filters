# EXPERIMENT 06:IMPLEMENTATION OF FILTERS
## AIM:
To implement filters for smoothing and sharpening the images in the spatial domain.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Import the necessary modules and read the image.
### Step 2:
Perform linear filtering operation.
### Step 3:
Apply following filters to the image for smoothing:
* Averaging filter
* Weighted Averaging Filter
* Gaussian Blur
* Median filter
### Step 4
Apply following filters to the image for sharpening:
* Laplacian kernel
* Laplacian operator
### Step 5: 
Display the image after applying filters.


## PROGRAM:
```
Developed By   : RITHIGA SRI.B
Register Number: 212221230083
````
### Importing libraries:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Smoothing Filters:

(i) Using Averaging Filter:
```
img1=cv2.imread('monument.jpg')
img2=cv2.cvtColor(img1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
img3=cv2.filter2D(img2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(img2)
plt.title('Original')
plt.axis('Off')
plt.subplot(1,2,2)
plt.imshow(img3)
plt.title("Filtered")
plt.axis("Off")
```

(ii) Using Weighted Averaging Filter:
```
kernel2=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
img3=cv2.filter2D(img2,-1,kernel2)
plt.imshow(img3)
plt.title("Weighted Averaging Filter")
plt.axis("Off")
```

(iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(src=img2,ksize=(11,11),sigmaX=0,sigmaY=0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blurring")
plt.axis("Off")
```

(iv) Using Median Filter
```
median=cv2.medianBlur(src=img2,ksize=11)
plt.imshow(median)
plt.title("Median Blurring")
plt.axis("Off")
```

### Sharpening Filters:
(i) Using Laplacian Kernal
```
kernel3=np.array([[0,1,0],[1,-4,1],[0,1,0]])
img3=cv2.filter2D(img2,-1,kernel3)
plt.imshow(img3)
plt.title("Laplacian kernel")
plt.axis("Off")
```
(ii) Using Laplacian Operator
```
new_img=cv2.Laplacian(img2,cv2.CV_64F)
plt.imshow(new_img)
plt.title("Laplacian Operator")
plt.axis("Off")
```

## OUTPUT:
### 1. Smoothing Filters:

(i) Using Averaging Filter
![image](https://user-images.githubusercontent.com/93427256/230083153-343030cf-0962-42cf-9394-514d13901922.png)

(ii) Using Weighted Averaging Filter
![image](https://user-images.githubusercontent.com/93427256/230083346-3e8c21a6-2e45-46f2-9508-dff3e3f02910.png)

(iii) Using Gaussian Filter
![image](https://user-images.githubusercontent.com/93427256/230083430-5f999c9d-f180-42e7-8dd4-78c0553509df.png)

(iv) Using Median Filter
![image](https://user-images.githubusercontent.com/93427256/230083548-760931cb-b28e-435a-b0e9-0837bcee9111.png)

### 2. Sharpening Filters:
(i) Using Laplacian Kernal
![image](https://user-images.githubusercontent.com/93427256/230083685-32728af5-6be5-4bde-a31b-c8b829982ef7.png)


(ii) Using Laplacian Operator
![image](https://user-images.githubusercontent.com/93427256/230083771-cca85adf-881a-4727-91dc-0a113dcced00.png)


## RESULT:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
