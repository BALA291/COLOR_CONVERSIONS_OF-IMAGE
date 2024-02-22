# EX-01 COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step 1: 
Choose an image and save it as a filename.jpg.
### Step 2: 
Use imread(filename, flags) to read the file.
### Step 3: 
Use imshow(window_name, image) to display the image.
### Step 4: 
Use imwrite(filename, image) to write the image.
### Step 5: 
End the program and close the output image windows.
### Step 6: 
Convert BGR and RGB to HSV and GRAY
### Step 7: 
Convert HSV to RGB and BGR
### Step 8: 
Convert RGB and BGR to YCrCb
### Step 9: 
Split and Merge RGB Image
### Step 10: 
Split and merge HSV Image

##### Program:
```
### Developed By: B.BALAMURUGAN
### Register Number: 212222230016
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
import cv2
import numpy as np
img=cv2.imread("bala.jpg")
img=cv2.resize(img,(400,300))
cv2.imshow("BALA",img)
cv2.waitKey(0)
``` 
  </td>
  <td>

### OUTPUT:

![o1](https://github.com/BALA291/COLOR_CONVERSIONS_OF-IMAGE/assets/120717501/878d7334-8e1b-4286-8554-b0cd17ff0f79)

  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
import cv2
img=cv2.imread('bala.jpg')
cv2.imwrite('bala.jpg',img)
```
  </td>
  <td>

### OUTPUT:

![o2](https://github.com/BALA291/COLOR_CONVERSIONS_OF-IMAGE/assets/120717501/9c4d899f-451a-4ed6-ae47-3d54dadd2260)

  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
import cv2
img=cv2.imread('bala.jpg')
print(img.shape)
```
  </td>
  <td>

### OUTPUT:
![o3](https://github.com/BALA291/COLOR_CONVERSIONS_OF-IMAGE/assets/120717501/c2cb485e-79e6-4b34-85a1-e2078c2e04af)


  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
import cv2
import random
img=cv2.imread('bala.jpg')
img=cv2.resize(img,(400,300))
for i in range(150,200):
    for j in range(img.shape[1]):
        img[i][j]=[random.randint(0,255),
                  random.randint(0,255),
                  random.randint(0,255)]
cv2.imshow('BALA',img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:
![o4](https://github.com/BALA291/COLOR_CONVERSIONS_OF-IMAGE/assets/120717501/7749a954-2237-4b68-8e6a-9d08c7f3b980)

  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
import cv2
img=cv2.imread('bala.jpg')
img=cv2.resize(img,(400,300))
tag=img[150:200,110:160]
img[110:160,150:200]=tag
cv2.imshow('bala',img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:

![o5](https://github.com/BALA291/COLOR_CONVERSIONS_OF-IMAGE/assets/120717501/0986740f-f6de-43c1-b895-7e5eae89cad6)

  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('bala.jpg',1)
img=cv2.resize(img,(400,300))
cv2.imshow('bala1',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![o6i](https://github.com/BALA291/COLOR_CONVERSIONS_OF-IMAGE/assets/120717501/5a9429da-612a-4dcc-a27d-acb41c645890)
![o6ii](https://github.com/BALA291/COLOR_CONVERSIONS_OF-IMAGE/assets/120717501/8be73f3d-1533-4a13-883b-7814af55ded7)



### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('bala.jpg')
img=cv2.resize(img,(400,300))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![o7](https://github.com/BALA291/COLOR_CONVERSIONS_OF-IMAGE/assets/120717501/7aae6acc-364a-4d56-8577-27e8871d2791)



### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('bala.jpg')
img=cv2.resize(img,(400,300))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![o8](https://github.com/BALA291/COLOR_CONVERSIONS_OF-IMAGE/assets/120717501/b789d4f4-4f90-45ac-8950-5436b1193063)



### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('bala.jpg')
img=cv2.resize(img,(400,300))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![o9i](https://github.com/BALA291/COLOR_CONVERSIONS_OF-IMAGE/assets/120717501/d6482206-ec61-411d-b090-107261d9f3e8)

![o9ii](https://github.com/BALA291/COLOR_CONVERSIONS_OF-IMAGE/assets/120717501/25daf117-de11-4c1a-9764-53a0c7cde683)




### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("bala.jpg")
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![o10](https://github.com/BALA291/COLOR_CONVERSIONS_OF-IMAGE/assets/120717501/7d27a2d6-5a9f-4a82-a933-6f555c4f9b86)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
