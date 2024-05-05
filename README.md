# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
 packages

### Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image


#### Step5: <br>
Dilate the Image

 
### Program:
```
NAME: ARCHANA K
REG.NO: 212222240011
```

##### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
##### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'ARCHANA',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
##### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
##### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
##### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
### Output:
#### Display the input Image

![Screenshot (139)](https://github.com/22009150/erosion--dilation/assets/118708624/88d4123a-59db-4f0e-bce1-3ebb420fe0b9)


#### Display the Eroded Image

![Screenshot (140)](https://github.com/22009150/erosion--dilation/assets/118708624/91b3b67b-33d8-4a59-b4f8-f43c1295321d)


#### Display the Dilated Image
![Screenshot (141)](https://github.com/22009150/erosion--dilation/assets/118708624/24e98465-5bae-49b4-9fdb-d7ba9e4f7660)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

