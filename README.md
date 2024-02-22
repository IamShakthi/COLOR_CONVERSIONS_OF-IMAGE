# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1: Choose an image and save it as a filename.jpg ,
### Step2: Use imread(filename, flags) to read the file.
### Step3: Use imshow(window_name, image) to display the image.
### Step4: Use imwrite(filename, image) to write the image.
### Step5: End the program and close the output image windows.
### Step6: Convert BGR and RGB to HSV and GRAY
### Step7: Convert HSV to RGB and BGR
### Step8: Convert RGB and BGR to YCrCb
### Step9: Split and Merge RGB Image
### Step10: Split and merge HSV Image

##### Program:
```
### Developed By: SRI KARTHICKEYAN GANAPATHY
### Register Number: 212222240102
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('dip.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('SRI KARTHICK',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:
![OUTPUT 1](https://github.com/IamShakthi/COLOR_CONVERSIONS_OF-IMAGE/assets/117913445/64c6b9be-a9be-4935-a3f8-4ac4cdae6834)


  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('dip.jpg',0)
    cv2.imwrite('demos.jpg',image)
```
  </td>
  <td>

### OUTPUT:

![OUTPUT 2](https://github.com/IamShakthi/COLOR_CONVERSIONS_OF-IMAGE/assets/117913445/9c258b2b-f534-463c-8643-74dc43ba0dd3)

  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('dip.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![OUTPUT 3](https://github.com/IamShakthi/COLOR_CONVERSIONS_OF-IMAGE/assets/117913445/2575f505-0638-418e-8b17-3a73099186e9)

  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
    import random
    import cv2
    image=cv2.imread('dip.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:

![OUTPUT 4](https://github.com/IamShakthi/COLOR_CONVERSIONS_OF-IMAGE/assets/117913445/1aab2778-24f5-449f-997a-501fc084c883)

  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
    import cv2
    image=cv2.imread('dip.jpg',1)
    image=cv2.resize(image,(400,400))
    tag =image[130:200,110:190]
    image[110:180,120:200] = tag
    cv2.imshow('partimage1',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:
![OUTPUT 5](https://github.com/IamShakthi/COLOR_CONVERSIONS_OF-IMAGE/assets/117913445/7ea18f6a-e369-4d40-8cf1-9573a1753700)



  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('dip.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
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

![OUTPUT 6](https://github.com/IamShakthi/COLOR_CONVERSIONS_OF-IMAGE/assets/117913445/20a67905-390a-4db6-b22f-19d2db9942d6)

### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('dip.jpg')
img = cv2.resize(img,(300,200))
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
![OUTPUT 7](https://github.com/IamShakthi/COLOR_CONVERSIONS_OF-IMAGE/assets/117913445/9c9ab4c3-87ac-46f5-b414-eacc68ccf53b)

### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('dip.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![OUTPUT 8](https://github.com/IamShakthi/COLOR_CONVERSIONS_OF-IMAGE/assets/117913445/e0ce74c0-1b40-49e4-a963-4dc057d01523)


### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('dip.jpg',1)
img = cv2.resize(img,(300,200))
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
![OUTPUT 9](https://github.com/IamShakthi/COLOR_CONVERSIONS_OF-IMAGE/assets/117913445/eeccafb7-d19f-4003-aa8a-f0b924adcef6)


### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("dip.jpg",1)
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
![OUTPUT 10](https://github.com/IamShakthi/COLOR_CONVERSIONS_OF-IMAGE/assets/117913445/5d134b82-5a7b-479c-9047-7978e6a76275)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







