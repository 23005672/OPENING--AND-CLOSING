# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Give the input text using cv2.putText().

### Step3:
Perform opening operation and display the result.

### Step4:
Similarly, perform closing operation and display the result.
 
## Program:
```
Developed by : RIYA P L
Register no  : 212223240141
```
``` Python
# Import the necessary packages
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'RIYA', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)

# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")

# Use Closing Operation
image2=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image
![Screenshot 2024-10-26 211623](https://github.com/user-attachments/assets/d453496a-0aaf-4d94-8a51-269e3e2baf5e)

### Display the result of Opening
![Screenshot 2024-10-26 211831](https://github.com/user-attachments/assets/e15abad5-d6e3-4819-91e4-bd0c1e661f00)

### Display the result of Closing
![Screenshot 2024-10-26 211842](https://github.com/user-attachments/assets/b9b2d0fd-8d46-4941-b79b-5e4b63c44926)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
