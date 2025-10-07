# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br> import the neccesary packages


### Step2:
<br> creat the text using cv2.put Text

### Step3:
<br> create the structuting element

### Step4:
<br>  Erodde the image

### Step5:
<br> Dilate the image
 
 
## Program:


``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt
imput_image='actor.jpg'
color_image=cv2.imread(imput_image)
gray_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
edges=cv2.Canny(gray_image,100,200)
kernel_size=5
kernel=np.ones((kernel_size,kernel_size),np.uint8)
erosion=cv2.erode(edges,kernel,iterations=1)
dilation=cv2.dilate(edges,kernel,iterations=1)
plt.figure(figsize=(15,10))
plt.subplot(2,3,1)
plt.imshow(cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
plt.subplot(2,3,2)
plt.imshow(gray_image,cmap='gray')
plt.title('black and white image')
plt.axis('on')
plt.subplot(2,3,3)
plt.imshow(edges,cmap='gray')
plt.title('edge segmentation')
plt.axis('on')
plt.subplot(2,3,4)
plt.imshow(edges,cmap='gray')
plt.title('erosion')
plt.axis('on')
plt.subplot(2,3,5)
plt.imshow(edges,cmap='gray')
plt.title('dilation')
plt.axis('on')




```
## Output:

<img width="310" height="326" alt="image" src="https://github.com/user-attachments/assets/f1c41149-57d7-4019-a4ea-fe94a6672efd" />
<img width="339" height="342" alt="image" src="https://github.com/user-attachments/assets/c7754ad0-1b44-4987-902b-72c5631fa6d2" />
<img width="308" height="329" alt="image" src="https://github.com/user-attachments/assets/bb504db4-584b-4033-ad41-52aea4031846" />



## Result:
Thus the generated text image is eroded and dilated using python and OpenCV.




