# Image-Transformation
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
Shear the image.

### Step5:
Find reflection of image.

### Step6:
Rotate the image.

### Step7:
Crop the image.

### Step8:
Display all the Transformed images.


## Program:
```python
Developed By: charumathi R
Register Number: 212222240021

i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("lion.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
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
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
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
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()




iv)Image Reflection
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("got.jpg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_yaxis)
plt.show()




v)Image Rotation
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("got.jpg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()



vi)Image Cropping

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("got.jpg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
cropped_img=input_image[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()



```
## Output:
### i)Image Translation
![165563682-2aba2243-4b07-45f5-a68d-5374ff78b6c7](https://user-images.githubusercontent.com/120204455/236689063-8c04b0d5-4dde-4e63-8a1a-a67364ed42c1.png)


### ii) Image Scaling
![165563720-04f4295f-8c7a-47ec-bbba-adca837b975a](https://user-images.githubusercontent.com/120204455/236689065-a5b721ab-a16c-4c5c-ab3c-f0460885468f.png)




### iii)Image shearing
![165563785-29f1c477-1dc4-45a3-a557-60bfcf748489](https://user-images.githubusercontent.com/120204455/236689069-f728c8a1-a855-4603-b54b-906fd08f1112.png)



### iv)Image Reflection
![165563834-8ed9e966-6dc6-4b6a-92af-24d4276d98df](https://user-images.githubusercontent.com/120204455/236689074-fe5b3bd3-7e4e-4d77-b18b-ed4bf02b6fa7.png)




### v)Image Rotation

![165563895-5572b9b1-39ef-4dfe-a255-a745f60d6ae4](https://user-images.githubusercontent.com/120204455/236689077-5f2139c4-84c4-4a60-9b3c-1ffaf2e2494f.png)



### vi)Image Cropping

![165563946-cb59a478-9d79-4703-97be-efe868472398](https://user-images.githubusercontent.com/120204455/236689087-53e58282-051e-4903-8ab9-7ebda45a77af.png)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
