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
### Smoothing Filters

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
```Python





```
iii) Using Gaussian Filter
```Python





```

iv) Using Median Filter
```Python





```

### Sharpening Filters
i) Using Laplacian Kernal
```Python





```
ii) Using Laplacian Operator
```Python





```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter
</br>
</br>
</br>
</br>
</br>

iii) Using Gaussian Filter
</br>
</br>
</br>
</br>
</br>

iv) Using Median Filter
</br>
</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
