# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:

```
Developed By: Adhithya.S
Register Number: 212222240003
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
image=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(image,'Adhithya S',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()


# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Use Opening operation
image2=cv2.morphologyEx(image,cv2.MORPH_OPEN,kernel)
plt.imshow(image2,cmap='gray')
plt.title('OPENING'), plt.xticks([]), plt.yticks([])
plt.show()



# Use Closing Operation
image3=cv2.morphologyEx(image,cv2.MORPH_CLOSE,kernel)
plt.imshow(image3,cmap='gray')
plt.title('CLOSING'), plt.xticks([]), plt.yticks([])
plt.show()




```
## Output:

### Display the input Image
![Screenshot 2023-10-18 104210](https://github.com/s-adhithya/OPENING--CLOSING/assets/113497423/1684d778-b158-46ad-8d92-03694db8bb4d)


### Display the result of Opening
![Screenshot 2023-10-18 104225](https://github.com/s-adhithya/OPENING--CLOSING/assets/113497423/75435578-d77f-4eeb-bbc2-ef58c6a4f59b)


### Display the result of Closing
![Screenshot 2023-10-18 104236](https://github.com/s-adhithya/OPENING--CLOSING/assets/113497423/0eec3f44-1cf7-4eca-a9e6-e987326c3eb1)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
