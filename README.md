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
DEVELOPED BY: G.Jayanth.
REGISTER NUMBER:212221230030
```
## Import the packages

``` Python
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dipex7.png")
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

<img width="421" alt="image" src="https://github.com/JayanthYadav123/EDGEDETECTION/assets/94836154/95be6b6c-51f1-4571-bd8e-f300033b9602">


# SOBEL Y:


<img width="416" alt="image" src="https://github.com/JayanthYadav123/EDGEDETECTION/assets/94836154/67478870-3575-427b-abd1-8868a6bd0030">


# SOBEL XY:


<img width="430" alt="image" src="https://github.com/JayanthYadav123/EDGEDETECTION/assets/94836154/2f179aca-3ce4-4b65-903d-3e75b48582d2">



### LAPLACIAN EDGE DETECTOR


<img width="449" alt="image" src="https://github.com/JayanthYadav123/EDGEDETECTION/assets/94836154/abae1a94-9f0b-44b3-8fdf-0fadfb012137">



### CANNY EDGE DETECTOR

<img width="431" alt="image" src="https://github.com/JayanthYadav123/EDGEDETECTION/assets/94836154/c8575912-4deb-4cc4-b6ef-5a1fd47512c9">


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
