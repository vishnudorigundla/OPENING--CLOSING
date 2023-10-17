# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages for implementing the code.
### Step2:
Create the text that you want to modify using opening and close filter.
### Step3:
Create the structuring element that you want to use over the image.
### Step4:
Apply the opening and closing operation for the original image.
### Step5:
Show the results using imshow function from cv2.

## Program:

``` Python
# Developed by: D. Vishnu vardhan reddy.
# Reg.No.: 212221230023
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_SCRIPT_COMPLEX
im=cv2.putText(img,' vishnu vardhan ',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(cv2.cvtColor(im, cv2.COLOR_BAYER_GR2BGRA))

# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(img,cv2.MORPH_OPEN,Kernel)
plt.imshow(cv2.cvtColor(image1, cv2.COLOR_BAYER_GR2BGRA))

# Use Closing Operation
image1=cv2.morphologyEx(img,cv2.MORPH_CLOSE,Kernel)
plt.imshow(cv2.cvtColor(image1,cv2.COLOR_BAYER_GR2BGRA))

```
## Output:

### Display the input Image
![image](https://github.com/vishnudorigundla/OPENING--CLOSING/assets/94175324/603d193c-5740-460d-939f-9fb6d764b449)

### Display the result of Opening
![image](https://github.com/vishnudorigundla/OPENING--CLOSING/assets/94175324/393d4576-c6a8-4077-b82c-cf477f8b9f03)

### Display the result of Closing

![image](https://github.com/vishnudorigundla/OPENING--CLOSING/assets/94175324/ba096223-076c-4868-abe0-3d0c71f8fa2a)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.







