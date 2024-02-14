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
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:
### Register Number: 




### i) Read and display the image
```
import cv2
img=cv2.imread("earth.jpg")
cv2.imshow("Earth",img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot (2)](https://github.com/Harish2404lll/COLOR_CONVERSIONS_OF-IMAGE/assets/141472096/bfeef1b3-182c-4336-96e1-af8ddd090b51)


### ii)Write the image
```
import cv2
img=cv2.imread("nature.jpg")
cv2.imwrite("Earth.jpg",img)
```
## Output:
![Screenshot 2024-02-14 111733](https://github.com/Harish2404lll/COLOR_CONVERSIONS_OF-IMAGE/assets/141472096/7d8f6795-7318-4881-84ad-63283af132db)


### iii)Shape of the Image
```
import cv2
img=cv2.imread("nature.jpg")
print(img.shape)
```
## Output:
![Screenshot 2024-02-14 111759](https://github.com/Harish2404lll/COLOR_CONVERSIONS_OF-IMAGE/assets/141472096/ff52c87e-6549-4175-90d6-f95109802001)


### iv)Access rows and columns
```
import cv2
import random
img=cv2.imread("nature.jpg")
img=cv2.resize(img,(400,400))
for i in range (150,200):
    for j in range(img.shape[1]):
        img[i][j]=[random.randint(0,255),
                   random.randint(0,255),
                   random.randint(0,255)]
cv2.imshow("image",img)
cv2.waitKey()
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-14 111837](https://github.com/Harish2404lll/COLOR_CONVERSIONS_OF-IMAGE/assets/141472096/68ddde4c-43ca-4778-ad51-5a0b8b16de5c)



### v)Cut and paste portion of image
```
import cv2
img=cv2.imread("nature.jpg",1)
x=0
y=0
x1=50
y1=150
x2=50
y2=100
crp=img[x:x1+x1,y:y2+y2]
cv2.imshow("original",img)
cv2.imshow("cropping",crp)
cv2.waitKey()
cv2.destroyAllWindows()
```
## Output:
![Screenshot (3)](https://github.com/Harish2404lll/COLOR_CONVERSIONS_OF-IMAGE/assets/141472096/0cae4a34-e754-4e4e-b092-201ed442d5fb)


### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('nature.jpg',1)
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
## Output:
![Screenshot 2024-02-14 112337](https://github.com/Harish2404lll/COLOR_CONVERSIONS_OF-IMAGE/assets/141472096/97a28c9e-f3ad-4fe0-9dba-b5507fb43c2f)



### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('nature.jpg')
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
## Output:
![Screenshot 2024-02-14 112505](https://github.com/Harish2404lll/COLOR_CONVERSIONS_OF-IMAGE/assets/141472096/1bf9671e-be2e-46aa-bd0d-0cb9740e1985)


### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('nature.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-14 112611](https://github.com/Harish2404lll/COLOR_CONVERSIONS_OF-IMAGE/assets/141472096/8a4ae1ff-f623-474c-903f-01887db28c98)


### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('nature.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-14 112611](https://github.com/Harish2404lll/COLOR_CONVERSIONS_OF-IMAGE/assets/141472096/9f4686de-492f-4b78-8d26-481236ed77a9)


### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("nature.jpg",1)
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
## Output:
![Screenshot 2024-02-14 113204](https://github.com/Harish2404lll/COLOR_CONVERSIONS_OF-IMAGE/assets/141472096/0e104e85-a7ba-449a-8e10-76fa6bb23920)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







