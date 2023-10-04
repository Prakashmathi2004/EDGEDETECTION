# EDGE-DETECTION
## AIM:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step1:
Import the required packages for further process.


### Step2:
Read the image and convert the bgr image to gray scale image.

### Step3:
Use gaussian filter for smoothing the image to reduce the noise.
### Step4:
Apply the respective filters - Sobel, Laplacian edge dectector and Canny edge dector.

### Step5:
Display the filtered image using plot and imshow.

 
## PROGRAM:
Developed by : PERARASU M

Register number : 212222100033

### ORIGINAL IMAGE:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("berrypie.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
```
```
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
```
### SOBEL EDGE DETECTOR
### Sobel X:
```
sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'RdPu')
plt.title('RdPu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()
```

### Sobel Y:
```
sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()
```


### Sobel XY:
```
sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'BuPu')
plt.title('BuPu')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'BuPu')
plt.title('Sobel XY')
plt.xticks([])
plt.yticks([])
plt.show()
```

### LAPLACIAN EDGE DETECTOR:
```
laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()
```


### CANNY EDGE DETECTOR:
```
canny_edge = cv2.Canny(new_image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'gist_gray')
plt.title('gist_gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gist_gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()
```

## OUTPUT:
### ORIGINAL IMAGE:
![image](https://github.com/PERARASU10/EDGEDETECTION/assets/118348589/ebfb8882-aa79-47d5-99e5-bed6e690375d)


<br>
</br>

### SOBEL EDGE DETECTOR
### Sobel X:
![image](https://github.com/PERARASU10/EDGEDETECTION/assets/118348589/41d8e53e-6b00-4151-8e3b-ec11f24efd2e)

<br>
</br>

### Sobel Y:
![image](https://github.com/PERARASU10/EDGEDETECTION/assets/118348589/677f449a-7de5-42d5-9bd2-f6223657c7d7)

<br>
</br>

### Sobel XY:
![image](https://github.com/PERARASU10/EDGEDETECTION/assets/118348589/e377cd46-39a5-4720-bfe3-4022ada510ad)

<br>
</br>

### LAPLACIAN EDGE DETECTOR:
![image](https://github.com/PERARASU10/EDGEDETECTION/assets/118348589/5d8931b8-affd-443b-a8d9-12b697d6f635)

<br>
</br>

### CANNY EDGE DETECTOR:
![image](https://github.com/PERARASU10/EDGEDETECTION/assets/118348589/e712e990-a121-461b-be80-c33f4b699e78)

## Result:
Thus, the edges are detected using Sobel, Laplacian, and Canny edge detectors.
