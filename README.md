# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

Import the required packages for further process.

### Step2:
<br>

Read the image and convert the rgb image to gray scale image.

### Step3:
<br>

Use filters for smoothing the image to reduce the noise.

### Step4:
<br>

Apply the respective filters - Sobel, Laplacian edge detector and Canny edge detector.

### Step5:
<br>

Display the filtered image using plot and imshow.

## Program:
```
DEVELOPED BY:PRAKASH M
REGISTER NUMBER:212222100035
```
## Import the packages

``` Python
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("d.png")
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
```
## SOBEL EDGE DETECTOR
## SOBEL X:
```python
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
SOBEL Y:
```python
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
SOBEL XY:
```python
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
## LAPLACIAN EDGE DETECTOR
```python
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
## CANNY EDGE DETECTOR

```python
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


## Output:
### SOBEL EDGE DETECTOR
# SOBEL X:

<img width="419" alt="image" src="https://github.com/Prakashmathi2004/EDGEDETECTION/assets/118350045/66c302c9-a569-4e5a-9f14-92dbe3303bc4">


# SOBEL Y:

<img width="425" alt="image" src="https://github.com/Prakashmathi2004/EDGEDETECTION/assets/118350045/db176231-4d07-47de-85af-46d2fee1be68">

# SOBEL XY:

<img width="425" alt="image" src="https://github.com/Prakashmathi2004/EDGEDETECTION/assets/118350045/433cad19-de4e-418f-8439-7504ec723bac">

### LAPLACIAN EDGE DETECTOR

<img width="431" alt="image" src="https://github.com/Prakashmathi2004/EDGEDETECTION/assets/118350045/2f56bb4a-5a2c-4661-b4f7-fe6f785c75c3">

### CANNY EDGE DETECTOR

<img width="425" alt="image" src="https://github.com/Prakashmathi2004/EDGEDETECTION/assets/118350045/a8b16f37-0e31-479a-92e9-8c36ae62e6cc">


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
