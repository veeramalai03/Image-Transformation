## Ex no: 5
## Date: 27/4/2022
# <p align="center">Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
<br>Translate the image using
M=np.float32([[1,0,20],[0,1,50],[0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step3:
<br>Scale the image using
M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step4:
<br>Shear the image using
M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step5:
<br>Reflection of image can be achieved through the code
M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step6:
Rotate the image using
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step 7:
Crop the image using
cropped_img=input_img[20:150,60:230]

### Step 8:
Display all the Transformed images.

## Program:
```python
Developed By:VEERAMALAI S
Register Number:212220230056

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("breakingbad.jpg")
input_image = cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape

i)Image Translation
M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()


ii) Image Scaling
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()



iii)Image shearing
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()


iv)Image Reflection
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()




v)Image Rotation

angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()



vi)Image Cropping
cropped_img=input_image[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()





```
## Output:
### i)Image Translation
<br>![sfe](https://user-images.githubusercontent.com/75234790/167680731-d4062122-66e1-416e-b1c1-85d247821741.png)

<br>
<br>
<br>

### ii) Image Scaling
<br>![sdgfsdg](https://user-images.githubusercontent.com/75234790/167680738-e0a7bb9a-77e8-4405-a191-6d96705a86f7.png)

<br>
<br>
<br>


### iii)Image shearing
<br>![Screenshot 2022-05-10 221346](https://user-images.githubusercontent.com/75234790/167680776-7c2cc6b4-e5b3-41c9-9c7d-9c9a1decad58.png)

<br>
<br>
<br>


### iv)Image Reflection
<br>![dfshg](https://user-images.githubusercontent.com/75234790/167680791-bc4d6623-f42e-44d8-a8cb-9d4d92d15154.png)

<br>
<br>



### v)Image Rotation
<br>![sdfdf](https://user-images.githubusercontent.com/75234790/167680817-5f672b3a-fa22-4472-89ad-e1ae30720103.png)

<br>
<br>



### vi)Image Cropping
<br>![serdtfg](https://user-images.githubusercontent.com/75234790/167680831-210d961b-1840-4408-9932-b345ff2bc58d.png)

<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
