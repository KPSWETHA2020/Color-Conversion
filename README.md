# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg

### Step2:
Use imread(filename, flags) to read file

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another

### Step4:
Split and merge the image using cv2.split and cv2.merge commands

### Step5:
End the program and close the output image windows.

## Program:
```python
# Developed By: Swethas.k.p
# Register Number: 212220230053
# i) Convert BGR and RGB to HSV and GRAY

import cv2
color_image = cv2.imread('Heidi.jpg')
cv2.imshow('Original image',color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()



# ii)Convert HSV to RGB and BGR
import cv2
color_image = cv2.imread('Heidi.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()




# iii)Convert RGB and BGR to YCrCb
import cv2
color_image = cv2.imread('Heidi.jpg')
cv2.imshow('Original image',color_image)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()



# iv)Split and Merge RGB Image
import cv2
image = cv2.imread('Heidi.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()



# v) Split and merge HSV Image
import cv2
image = cv2.imread('Heidi.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()



```
## Output:
### i) BGR and RGB to HSV and GRAY
![ss1](https://user-images.githubusercontent.com/75235209/163677836-8446e46f-3d68-484a-8c80-445f72ab248a.PNG)


### ii) HSV to RGB and BGR
![ss2](https://user-images.githubusercontent.com/75235209/163677888-5313b82e-7bd0-469b-ab94-eda848889aff.PNG)


### iii) RGB and BGR to YCrCb
![ss3](https://user-images.githubusercontent.com/75235209/163677991-2a63644c-62b1-463c-8ce7-ff9f7e599e2f.PNG)


### iv) Split and merge RGB Image
![ss4](https://user-images.githubusercontent.com/75235209/163678005-ab33671e-1798-45f7-a968-81b41a06ab27.PNG)


### v) Split and merge HSV Image
![image](https://user-images.githubusercontent.com/75235209/163678096-68fe6da4-4cee-4f8c-a14b-6eac25f012f0.png)
![image](https://user-images.githubusercontent.com/75235209/163678173-50e33ecb-c909-46f5-9a35-21b65dfd9d80.png)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
