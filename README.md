# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it a image variable.
<br>

### Step2:
Translate the image using
Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]]) Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))
<br>

### Step3:
Scale the image using
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]]) Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))
<br>

### Step4:
Shear the image using
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]]) Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col2,int(row1.5)))
<br>

### Step5:
Reflection of image can be achieved through the code
Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]]) Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))
<br>

### Step6:
Rotate the image using
Rotation_angle=np.radians(10) Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0], [np.sin(Rotation_angle),np.cos(Rotation_angle),0], [0,0,1]]) Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))
<br>

### Step7:
Crop the image using
cropped_image=org_img[10:350,320:560]
<br>

### Step8:
Display all the Transformed images.
<br>


## Program:
```python
Developed By:Gowri M
Register Number:212220230019  
import cv2
import numpy as np
import matplotlib.pyplot as plt
original_img=cv2.imread("image.jpeg")
original_img=cv2.cvtColor(original_img,cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(original_img)
row,col,dim=original_img.shape

i)Image Translation
Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]])
Translated_image=cv2.warpPerspective(original_img,Translation_matrix,(col,row))
plt.axis("off")
plt.imshow(Translated_image)

ii) Image Scaling
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
Scaled_image=cv2.warpPerspective(original_img,Scaling_Matrix,(col,row))
plt.axis("off")
plt.imshow(Scaled_image)

iii)Image Shearing
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
Sheared_image=cv2.warpPerspective(original_img,Shearing_matrix,(col*2,int(row*1.5)))
plt.axis("off")
plt.imshow(Sheared_image)

iv)Image Reflection
Reflection_matrix_col=np.float32([[-1,0,col],[0,1,0],[0,0,1]])
Reflected_image_col=cv2.warpPerspective(original_img,Reflection_matrix_col,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_col)

Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]])
Reflected_image_row=cv2.warpPerspective(original_img,Reflection_matrix_row,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_row)

v)Image Rotation
Rotation_angle=np.radians(10)
Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0],
                                [np.sin(Rotation_angle),np.cos(Rotation_angle),0],
                                [0,0,1]])
Rotated_image=cv2.warpPerspective(original_img,Rotation_matrix,(col,(row)))
plt.axis("off")
plt.imshow(Rotated_image)

vi)Image Cropping
cropped_image=original_img[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_image)

```
## Output:
### i)Image Translation
![o1di](https://user-images.githubusercontent.com/75235455/165481262-e935410f-9de6-449d-934c-24fc057de140.png)
<br>
<br>
<br>
<br>

### ii) Image Scaling
![o2di](https://user-images.githubusercontent.com/75235455/165481401-b38f7fdc-0a68-40b4-b289-49029d530815.png)
<br>
<br>
<br>
<br>


### iii)Image shearing
![o3di](https://user-images.githubusercontent.com/75235455/165481468-818878df-6f66-485a-a6b2-ae4583dc99fa.png)
<br>
<br>
<br>
<br>


### iv)Image Reflection
![o4di](https://user-images.githubusercontent.com/75235455/165481571-31a1e5f2-61d4-4865-ba1e-fa482976dff1.png)
![o41di](https://user-images.githubusercontent.com/75235455/165481601-530321c7-68ad-4269-8b96-768a19ec74ec.png)
<br>
<br>
<br>
<br>



### v)Image Rotation
![o5di](https://user-images.githubusercontent.com/75235455/165481653-b43c3ab4-5fc4-496f-9e9b-f6fd8ca6dbc9.png)
<br>
<br>
<br>
<br>



### vi)Image Cropping
![o6d](https://user-images.githubusercontent.com/75235455/165481947-a94a406e-b85c-4d7a-8420-38a507455dee.png)
<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
