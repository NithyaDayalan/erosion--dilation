## Implementation-of-Erosion-and-Dilation

### Aim :
To implement Erosion and Dilation using Python and OpenCV.

### Software Required :
1. Anaconda - Python 3.7
2. OpenCV
   
### Algorithm :
#### Step 1 :
Create a blank image using numpy
#### Step 2 :
Add text with cv2.putText
#### Step 3 :
Define a 3x3 kernel
#### Step 4 :
Apply erosion to shrink text
#### Step 5 :
Apply dilation to expand text and display images.

### Program :
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hello Nithya', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create the structuring element
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) 
plt.title("Input Image with Text")
plt.axis('off')

# Erode the image
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  
plt.title("Eroded Image")
plt.axis('off')

# Dilate the image
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  
plt.title("Dilated Image")
plt.axis('off')
```

### Output :
#### Input Image :
<img width="663" height="534" alt="image" src="https://github.com/user-attachments/assets/3d3abb63-b2ec-49db-8bbc-938e87ae852c" />

#### Eroded Image :
<img width="671" height="539" alt="image" src="https://github.com/user-attachments/assets/75e19de8-c30f-4de8-a3d7-ff22c518136d" />

#### Dilated Image :
<img width="680" height="536" alt="image" src="https://github.com/user-attachments/assets/5670273c-4593-434c-9555-47e24df2f279" />

### Result :
Thus the generated text image is eroded and dilated using python and OpenCV.
