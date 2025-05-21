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

### Developed by: Karsavarthan R R
### Reg NO: 212223230100

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

![Screenshot 2025-05-21 210725](https://github.com/user-attachments/assets/c666abdc-9f4d-4f06-bfd2-fea3c4457c3f)


### Display the Eroded Image

![Screenshot 2025-05-21 210737](https://github.com/user-attachments/assets/cc61466c-ecd5-4014-8250-ae050798b285)


### Display the Dilated Image

![Screenshot 2025-05-21 210751](https://github.com/user-attachments/assets/e0dac23e-6136-49b0-8030-d210b7399a5e)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
