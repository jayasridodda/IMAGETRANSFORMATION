# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image.

### Step3:
Scale the image.

### Step4:
Shear the image in both the the axes.

### Step5:
Find the reflection of the image.

### Step6:
Rotate the image.

### Step7:
Crop the image.

### Step8:
Display all the transformed images.


## Program:
```python
Developed By: JAYASRI DODDA
Register Number: 212222240028
```
## Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("ex5p.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
translated_image = cv2.warpPerspective(org_image,M,(cols,rows))
plt.imshow(translated_image)
plt.show()
```
## Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("ex5p.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```
## Image Shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("ex5p.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```
## Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("ex5p.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
## Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("ex5p.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
angle = np.radians(25)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(org_image,M,(int(cols),int(rows)))
plt.imshow(rotated_img)
plt.show()
```
## Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("ex5p.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation
![Screenshot from 2023-09-09 16-06-19](https://github.com/jayasridodda/IMAGETRANSFORMATION/assets/123259278/aa8ad8cd-5460-48a6-a9e8-a07c05e29bfa)

### ii) Image Scaling
![Screenshot from 2023-09-09 16-06-27](https://github.com/jayasridodda/IMAGETRANSFORMATION/assets/123259278/c83678f8-78ed-4068-8953-3a5612673894)


### iii)Image shearing
![Screenshot from 2023-09-09 16-06-35](https://github.com/jayasridodda/IMAGETRANSFORMATION/assets/123259278/44cbfc88-75c9-4f3b-9973-f72ee9d2c99f)
![Screenshot from 2023-09-09 16-06-47](https://github.com/jayasridodda/IMAGETRANSFORMATION/assets/123259278/cc1ef38d-5c00-4123-8919-f8c1e405b831)

### iv)Image Reflection
![Screenshot from 2023-09-09 16-07-08](https://github.com/jayasridodda/IMAGETRANSFORMATION/assets/123259278/2dbf21e7-0748-4add-b9fa-87a65d7c42e8)
![Screenshot from 2023-09-09 16-07-18](https://github.com/jayasridodda/IMAGETRANSFORMATION/assets/123259278/6ecc8308-b0b9-49c8-88d4-908a90d2add0)

### v)Image Rotation
![Screenshot from 2023-09-09 16-07-30](https://github.com/jayasridodda/IMAGETRANSFORMATION/assets/123259278/90c1705a-b174-41f3-9834-d4020a2f386e)

### vi)Image Cropping
![Screenshot from 2023-09-09 16-07-40](https://github.com/jayasridodda/IMAGETRANSFORMATION/assets/123259278/04518e56-c541-4205-bef9-3f6765162a15)

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
