# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import the necessary libraries and read the original image and save it as a image variable.

## Step2:
Translate the image.

## Step3:
Scale the image.

## Step4:
Shear the image.

## Step5:
Find reflection of image.

## step6:
Rotate the image.

## Step7:
Crop the image.

## Step8:
Display all the Transformed images.

## Program:
```
Developed By:NIROSHA S
Register Number:212222230097
```
i)Image Translation:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image = cv2.warpPerspective(lion_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
```
ii) Image Scaling:

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
scaled_img = cv2.warpPerspective(lion_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

```
```
iii)Image shearing:

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```
```
iv)Image Reflection:

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
dog_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```
```
v)Image Rotation:

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(lion_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```
```
vi)Image Cropping:

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
cropped_img=lion_image[11:500,27:630]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()


```
## Output:
### i)Image Translation
![Screenshot from 2023-09-13 14-41-59](https://github.com/Niroshassithanathan/IMAGETRANSFORMATION/assets/121418437/852512ac-091f-4b12-bbe8-3e4a726b27c6)


### ii) Image Scaling

![Screenshot from 2023-09-13 14-42-49](https://github.com/Niroshassithanathan/IMAGETRANSFORMATION/assets/121418437/eae1d975-036c-4244-921a-6fefbdb814c6)


### iii)Image shearing
![Screenshot from 2023-09-13 14-43-37](https://github.com/Niroshassithanathan/IMAGETRANSFORMATION/assets/121418437/ad726263-db83-4349-b209-9934cb7e8838)
![Screenshot from 2023-09-13 14-43-46](https://github.com/Niroshassithanathan/IMAGETRANSFORMATION/assets/121418437/71e90d24-990c-48c9-816d-645505aecd90)
![Screenshot from 2023-09-13 14-43-56](https://github.com/Niroshassithanathan/IMAGETRANSFORMATION/assets/121418437/9be12b49-b618-45c0-a7bc-d13dd3fcfd31)


### iv)Image Reflection
![Screenshot from 2023-09-13 14-44-46](https://github.com/Niroshassithanathan/IMAGETRANSFORMATION/assets/121418437/efa1df73-e377-4995-8aae-63b9ef01307b)
![Screenshot from 2023-09-13 14-44-55](https://github.com/Niroshassithanathan/IMAGETRANSFORMATION/assets/121418437/1f6243ab-1300-4a3f-9a4d-39d12170e8ca)
![Screenshot from 2023-09-13 14-45-06](https://github.com/Niroshassithanathan/IMAGETRANSFORMATION/assets/121418437/a2bebcfd-791b-4862-bc5b-461595f3782a)



### v)Image Rotation
![Screenshot from 2023-09-13 14-45-15](https://github.com/Niroshassithanathan/IMAGETRANSFORMATION/assets/121418437/d60c8cbe-97e9-4689-98de-6b605e2e2134)


### vi)Image Cropping
![Screenshot from 2023-09-13 14-45-30](https://github.com/Niroshassithanathan/IMAGETRANSFORMATION/assets/121418437/34aa18e7-d6b0-44d7-a32c-eef21a4494cf)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
