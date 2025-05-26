# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>
Initialize an Empty Image:Create a black image of size 100x600 pixels.
### Step2:
<br>
Add Text to the Image:Use a specified font to write the word "Lifestyle" on the image at a defined position.
### Step3:
<br>
Display the Original Image:Show the image containing the text without axis labels.

### Step4:
<br>
Create Structuring Elements:Define a structuring element for morphological operations (e.g., a cross-shaped kernel).

### Step5:
<br>
Erode the Image:Apply erosion to the image using the defined structuring element to reduce the size of white regions.
### Step-6
Dilate the Image:Apply dilation to the original image using the same structuring element to increase the size of white regions.
 
## Program:


``` Python
Developed by : SRIVATSAN G
Register Number : 212223230216
```
# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
image = np.zeros((300, 600, 3), dtype="uint8")
text = "JACK"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 1, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```
# Erode the image
````
eroded_image = cv2.erode(image, kernel, iterations=1)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 1,1)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")
````
# Dilate the image
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 1,1)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
```
## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/f9ff3564-78db-439c-893c-1635caaac043)

### Display the Eroded Image
![image](https://github.com/user-attachments/assets/cb06a8a7-a289-42eb-9570-32c8ff61de08)

### Display the Dilated Image
![image](https://github.com/user-attachments/assets/c58a4453-dd4d-4796-8718-98139f8f1320)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
