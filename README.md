# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
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
 
## Program:

``` 
Developed by : M VIDYA NEELA
Reg no : 212221230120
```

# Original img:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("pup.jpeg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
```

# SOBEL EDGE DETECTOR
### sobel x:
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

### sobel y:
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
### sobel xy:
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

# LAPLACIAN EDGE DETECTOR:
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




# CANNY EDGE DETECTOR
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

## Output:
### Original img:

![image](https://user-images.githubusercontent.com/94169318/231820471-648b3f52-c059-4164-8794-ef0968c39a0c.png)


### SOBEL EDGE DETECTOR
### sobel x:
![image](https://user-images.githubusercontent.com/94169318/231820669-191f629c-3326-4f7e-bb13-6c3deb747744.png)

### sobel y:

![image](https://user-images.githubusercontent.com/94169318/231820803-d2beb6dc-9151-43f5-849c-57ed3238cd81.png)

### sobel xy:

![image](https://user-images.githubusercontent.com/94169318/231820954-fd3d29ad-7edd-44b9-83f3-aaa9d22c9dec.png)


### LAPLACIAN EDGE DETECTOR

![image](https://user-images.githubusercontent.com/94169318/231821007-e90f84cb-061d-4047-9b11-7fb03bd290d0.png)



### CANNY EDGE DETECTOR

![image](https://user-images.githubusercontent.com/94169318/231821092-cc43d72d-1251-4945-94be-bba35e69a663.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
