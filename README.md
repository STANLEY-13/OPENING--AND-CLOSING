# OPENING--AND-CLOSING
### Name: STANLEY S
### Ref no: 212223110054
## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:
Similarly, perform closing operation and display the result

 
## Program:

Python
``` 
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create a blank image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
# Add text on the image using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Amruthavarshini', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
# Create a simple square kernel (3x3)
```
kernel = np.ones((3, 3), np.uint8)
```
# Display the input image
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
# Opening is erosion followed by dilation
```
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
```
# Display the result of Opening
```
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
```
# Closing is dilation followed by erosion
```
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(closed_image)
plt.axis("off")
```

## Output:




### Display the result of Opening
<br>
<br>
<br>

<img width="389" height="411" alt="a33c0799-abd4-4f10-a56b-0c9098345be0" src="https://github.com/user-attachments/assets/33201f56-ee90-448b-b822-b819f5925550" />



<br>
<br>
<br>

### Display the result of Closing
<br>
<br>
<br>

<img width="389" height="411" alt="288e80e6-2251-4972-bc7e-5853a0160ba3" src="https://github.com/user-attachments/assets/fef0dfff-5364-4f2d-b0d8-523dac726a20" />



<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
