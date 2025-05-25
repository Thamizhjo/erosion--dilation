# EXP 09
# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale

### Step2:
Define a structuring element (kernel) for morphological operations.

### Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.

### Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.

### Step5:
Display and compare the original, eroded, and dilated images.
 
## Program:

### Developed by: THAMIZH KUMARAN S
### Reg NO: 212223240166

``` Python

import cv2
import numpy as np
from matplotlib import pyplot as plt

img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

cv2.putText(img1,'KARSA' ,(5,70),font,4,(255),2,cv2.LINE_AA)

kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')

```
## Output:

### Display the input Image
![Screenshot 2025-05-26 002104](https://github.com/user-attachments/assets/fe3f2896-bdf8-460d-b617-10ffad9793cb)




### Display the Eroded Image

![Screenshot 2025-05-26 002107](https://github.com/user-attachments/assets/ace7351f-3927-4c63-b2b5-b271419530ea)


### Display the Dilated Image

![Screenshot 2025-05-26 002111](https://github.com/user-attachments/assets/1bd99daf-1cec-4ad2-a2f9-669db991b6c4)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
