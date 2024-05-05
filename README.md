# EX-9 Implementation of Erosion and Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText
### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

 
## Program:

# Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'HEALTH',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```


# Create the structuring element
```python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```


# Erode the image

```python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```

# Dilate the image
```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')

```
## Output:

### Display the input Image
![325469228-2ebe9cd7-b72b-44b8-a1e0-ac7aebc8af18](https://github.com/SandhiyaR1/erosion--dilation/assets/113497571/406c10ea-2e33-4c66-8bee-00e682c576d7)


### Display the Eroded Image
![325469261-d32b69aa-5004-4f63-8ffa-eeefe4db71b8](https://github.com/SandhiyaR1/erosion--dilation/assets/113497571/b7778ab7-0cae-4a9f-8a5c-014c9956c923)

### Display the Dilated Image

![325469801-d48d36d7-3621-4065-bc74-7ebf5e03f91b](https://github.com/SandhiyaR1/erosion--dilation/assets/113497571/5741e2d4-392b-4721-ac7f-0671a759db6d)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
