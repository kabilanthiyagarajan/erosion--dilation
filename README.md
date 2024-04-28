# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary libraries (OpenCV and NumPy).

### Step2:
Use cv2.putText to add the text to the img1 image at specific coordinates.

### Step3:
Define two kernels (kernel and kernel1) for morphological operations.

### Step4:
Display the eroded image using cv2.imshow.

### Step5:
Use cv2.waitKey(0) to wait for a key press indefinitely.
 
## Program:
```
DEVELOPED BY: kabilan T
REG NO: 212222230059
```
### Import the necessary packages
```
import cv2
import numpy as np
```
### Create the Text using cv2.putText
```
img1=np.zeros((100,400),dtype="uint8")
font=cv2.FONT_HERSHEY_PLAIN
cv2.putText(img1,"Buna Ziua",(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("image",img1)
cv2.waitKey(0)
```
### Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
### Erode the image
```
cv2.erode(img1, kernel)
image_erode = cv2.erode(img1,kernel1)
cv2.imshow("JAI",image_erode)
cv2.waitKey(0)
```
### Dilate the image
```
image_dilatel=cv2.dilate(img1,kernel1)
cv2.imshow("JAI",image_dilatel)
cv2.waitKey(0)
```
## Output:

### Display the input Image

![image](https://github.com/Ragu-123/erosion-dilation/assets/113915622/5be64cb3-a5b7-4c8f-94af-cefb750e316f)


### Display the Eroded Image

![image](https://github.com/Ragu-123/erosion-dilation/assets/113915622/2c6f4255-44e0-4a20-a8aa-8dc536373d3a)


### Display the Dilated Image
![image](https://github.com/Ragu-123/erosion-dilation/assets/113915622/a1c3f4d8-de8e-4f6f-9120-536d9625d6c1)




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
