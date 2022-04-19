# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
<br>
Import CV2 library.

### Step2:
<br>
Use cv2.cvtcolor() to convert colot in required image.

### Step3:
<br>
Use .imshow() to display and .imwrite() to save.

### Step4:
<br>
Use split() to disperse color into separate channels.

### Step5:
<br>
Use merge() to combine those separate channels into color.

## Program:
```python
# Developed By: G.Thirugnanamoorthi
# Register Number: 212221230117
# i) Convert BGR and RGB to HSV and GRAY

import cv2
house_color_image = cv2.imread('wp2767718.jpg')
cv2.imshow('Original image', house_color_image)
hsv_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (house_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()




# ii)Convert HSV to RGB and BGR

import cv2
house_color_image = cv2.imread('wp2767718.jpg')
cv2.imshow('Original image', house_color_image)
hsv_imagel = cv2.cvtColor(house_color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' , hsv_imagel)
gray_image = cv2.cvtColor(house_color_image, cv2.COLOR_HSV2BGR)
cv2.imshow( 'HSV2BGR', gray_image)
cv2.waitKey(0)
cv2. destroyAllWindows()



# iii)Convert RGB and BGR to YCrCb
import cv2
house_color_image = cv2.imread('wp2767718.jpg')
cv2.imshow('Original image', house_color_image)
hsv_imagel = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb' , hsv_imagel)
gray_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow( 'BGR2YCrCb', gray_image)
cv2.waitKey(0)
cv2. destroyAllWindows()



# iv)Split and Merge RGB Image
import cv2
image = cv2.imread('wp2767718.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red)
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()



# v) Split and merge HSV Image
import cv2
image = cv2.imread('wp2767718.jpg')
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
![1](https://user-images.githubusercontent.com/94980741/164015571-985fb8b4-08e1-4138-adb8-98781753c56c.png)

### i) BGR and RGB to HSV and GRAY
![2](https://user-images.githubusercontent.com/94980741/164015378-7ff04fed-b75b-47fd-b87f-22d897fdf1ce.png)
<br>
![3](https://user-images.githubusercontent.com/94980741/164015415-61f77d7e-19ae-4462-ad64-0080e7eaac5b.png)


### ii) HSV to RGB and BGR
![4](https://user-images.githubusercontent.com/94980741/164015623-3878763f-686a-4622-a37c-de695f5c96e0.png)
<br>
![5](https://user-images.githubusercontent.com/94980741/164015687-64a95dc9-09e1-4b37-94a8-87f24836c541.png)



### iii) RGB and BGR to YCrCb
![6](https://user-images.githubusercontent.com/94980741/164017664-633b7b54-30bb-44b2-b846-e5da6a3da547.png)

<br>
![7](https://user-images.githubusercontent.com/94980741/164015871-10e9d5ba-43fc-439f-8ed2-a3d6481d48c2.png)



### iv) Split and merge RGB Image
![B-Channel](https://user-images.githubusercontent.com/94980741/164015964-645dfa49-f41d-4fe2-9f9c-031a31efeda8.png)
<br>
![G-Channel](https://user-images.githubusercontent.com/94980741/164016006-a15e3564-e92b-4eaa-95a8-a5e35988c493.png)
<br>
![R-Channel](https://user-images.githubusercontent.com/94980741/164016052-dd1c92fe-cae7-4571-995f-fddcab3b7c88.png)



### v) Split and merge HSV Image
![Merged HSV Image](https://user-images.githubusercontent.com/94980741/164016111-b09f8cc5-219e-4cc3-aa6c-3500ca0b377b.png)
<br>
![Saturation-Image](https://user-images.githubusercontent.com/94980741/164016848-14388a82-a3f9-4996-af12-9f6ea0a414d3.png)
<br>
![Hue-Image](https://user-images.githubusercontent.com/94980741/164016909-a8048d28-8619-4d25-ba00-8174732ab5a9.png)




## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
