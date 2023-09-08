# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.
### Step2:
load the image file in the program.
### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using
OpenCV and Python.
### Step4:
Display the modified image output.
### Step5:
End the program.
## Program:
Developed By:bhuvaneshwari.S
Register Number:212221240010
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("aa.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(image)
plt.show()
rows,cols,dim = image.shape
## i)Image Translation
M = np.float32([[1,0,100],
[0,1,200],
[0,0,1]])
translated_image = cv2.warpPerspective(image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
## ii) Image Scaling
scaling_matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
scaled_img=cv2.warpPerspective(input,scaling_matrix,(cols,rows))
plt.axis("off")
plt.imshow(scaled_img)
## iii)Image shearing
M_x = np.float32([[1,0.5,0],
[0,1,0],
[0,0,1]])
M_y = np.float32([[1,0,0],
[0.5,1,0],
[0,0,1]])
sheared_xaxis = cv2.warpPerspective(image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_yaxis = cv2.warpPerspective(image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_yaxis)
plt.show()
## iv)Image Reflection
M_x = np.float32([[1,0.5,0],
[0,1,0],
[0,0,1]])
M_y = np.float32([[1,0,0],
[0.5,1,0],
[0,0,1]])
sheared_xaxis = cv2.warpPerspective(image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_yaxis = cv2.warpPerspective(image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_yaxis)
## v)Image Rotation
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],
[np.sin(angle),np.cos(angle),0],
[0,0,1]])
rotated_image = cv2.warpPerspective(image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_image)
plt.show()
## vi)Image Cropping
cropped_image = image[100:300,100:300]
plt.axis('off')
plt.imshow(cropped_image)
plt.show()
## Output:

![image](https://github.com/Bhuvaneshwari-2003/IMAGETRANSFORMATION/assets/94828604/15935212-ea4d-4226-bdfd-2f8d6ad8a4af)

### i)Image Translation:

![image](https://github.com/Bhuvaneshwari-2003/IMAGETRANSFORMATION/assets/94828604/10b9e3fa-9592-4c02-9674-e090cd83eef7)



### ii) Image Scaling:

![image](https://github.com/Bhuvaneshwari-2003/IMAGETRANSFORMATION/assets/94828604/e261b4f3-b7ad-4e57-81dc-f82f37d4d516)

### iii)Image shearing:

![image](https://github.com/Bhuvaneshwari-2003/IMAGETRANSFORMATION/assets/94828604/1db3d540-bd91-4f96-9881-02c53a6cd751)

### iv)Image Reflection:

![image](https://github.com/Bhuvaneshwari-2003/IMAGETRANSFORMATION/assets/94828604/858c1c42-4771-49c8-920f-9ff3a6837785)

### v)Image Rotation:

![image](https://github.com/Bhuvaneshwari-2003/IMAGETRANSFORMATION/assets/94828604/b1798bc0-2e24-41bb-9ef6-938f3c9b197d)

### vi)Image Cropping:

![image](https://github.com/Bhuvaneshwari-2003/IMAGETRANSFORMATION/assets/94828604/1e494ff0-0483-4637-a550-febb312bc89d)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
