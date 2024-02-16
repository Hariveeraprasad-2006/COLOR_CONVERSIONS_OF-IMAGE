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


## Output:

### i) Read and display the image
### code
```
import cv2
color_image=cv2.imread("TIGER image.jpg")
cv2.imshow("colorimage",color_image)
cv2.waitKey(0)
```
### IMAGE
![Screenshot 2024-02-16 111243](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/1bc65df4-7d0c-490b-bcd0-329345b24ccd)


### ii)Write the image
### code
```
import cv2
image=cv2.imread('TIGER image.jpg',0)
cv2.imwrite('new1.jpg',image)
```
### IMAGE
![image](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/f6181c69-90dc-4f59-b70c-87e97b0b26e9)

### iii)Shape of the Image
### code
```
import cv2
color_image=cv2.imread("TIGER image.jpg")
print(color_image.shape)
```
### IMAGE
![image](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/2bc0d415-ad95-447c-acd6-dc009129a327)

### iv)Access rows and columns
### CODE:
```
import random
import cv2
color_image=cv2.imread("TIGER image.jpg")
for i in range(100):
    for j in range(color_image.shape[1]):
        color_image[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2.imshow('part image',color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### IMAGE:
![Screenshot 2024-02-16 112118](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/bc065d93-8fe7-48ce-b38e-766d855ebd8e)

### v)Cut and paste portion of image
### CODE:
```
import cv2
color_image=cv2.imread("TIGER image.jpg")
tag=color_image[300:400,300:400]
color_image[50:150,50:150]=tag
cv2.imshow("partimage1",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### IMAGE
![Screenshot 2024-02-16 112638](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/b8c2668f-0207-4d49-9a9a-80d26decb56b)

### vi) BGR and RGB to HSV and GRAY
### CODE
```
import cv2
color_image=cv2.imread("TIGER image.jpg")
cv2.imshow("Original image",color_image)
hsv_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR2HSV",hsv_image)
hsv_image1=cv2.cvtColor(color_image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB2HSV",hsv_image1)
gray_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR2GRAY",gray_image)
gray_image1=cv2.cvtColor(color_image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB2GRAY",gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### IMAGE:
### BGR2HSV
![Screenshot 2024-02-16 113722](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/609ef88b-700a-4caf-8b2e-0e8e18671882)
### RGB2HSV
![Screenshot 2024-02-16 113640](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/0bd395b9-909e-4ab9-aa91-5f42ce578464)
### BGR2GRAY
![Screenshot 2024-02-16 113819](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/53d0b402-5a6d-4568-aa19-738c6b2da9da)
### RGB2GRAY
![Screenshot 2024-02-16 113831](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/a2b2c934-1d4d-4d59-b360-2d974c54757b)

### vii) HSV to RGB and BGR
### CODE:
```
import cv2
color_image=cv2.imread("TIGER image.jpg")
cv2.imshow("Original HSV image",color_image)
RGB_image=cv2.cvtColor(color_image,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV2RGB",RGB_image)
BGR_image1=cv2.cvtColor(color_image,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV2BGR",BGR_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### IMAGE:
# HSV2BGR
![Screenshot 2024-02-16 114256](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/08fca151-a8b4-43fa-b178-a006c970c588)
# HSV2RGB::
![Screenshot 2024-02-16 114316](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/74cd8335-da4c-4eab-84fc-763b86e64b71)

### viii) RGB and BGR to YCrCb
### CODE:
```
import cv2
color_image=cv2.imread("TIGER image.jpg")
cv2.imshow("Original HSV image",color_image)
YCrCb_image1=cv2.cvtColor(color_image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB2YCrCb",YCrCb_image1)
YCrCB_image2=cv2.cvtColor(color_image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR2YCrYb",YCrCB_image2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### IMAGE:
# COLOR_BGR2YCrCb
![Screenshot 2024-02-16 114850](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/b2d50ce1-7e08-4182-8489-5aafa943d650)
# COLOR_RGB2YCrCb:
![Screenshot 2024-02-16 114907](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/b14c27aa-9651-41dd-8625-1c429968c99c)

### ix) Split and merge RGB Image
### CODE:
```
import cv2
color_image=cv2.imread("TIGER image.jpg")
RGB_image=cv2.cvtColor(color_image,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV2RGB",RGB_image)
blue=color_image[:,:,0]
green=color_image[:,:,1]
red=color_image[:,:,2]
cv2.imshow("blue",blue)
cv2.imshow("green",green)
cv2.imshow("red",red)
merge_show=cv2.merge((blue,green,red))
cv2.imshow("MERGED",merge_show)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# IMAGE:
# RED:
![Screenshot 2024-02-16 115509](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/41970c00-47df-4ef7-872c-a85c1a346d8a)
# GREEN:
![Screenshot 2024-02-16 115609](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/5e0fe872-6e58-4471-b59f-67a51b841dfb)
# BLUE:
![Screenshot 2024-02-16 115626](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/0ae9e30e-5c34-413e-a1cc-cb914bd1a6f7)
# MERGED IMAGE:
![Screenshot 2024-02-16 120132](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/c66d7b1e-dee9-454a-a3ea-8563d637ea52)


### x) Split and merge HSV Image
### CODE:
```
import cv2
color_image=cv2.imread("TIGER image.jpg")
hsv_image=cv2.cvtColor(color_image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB2HSV",hsv_image)
h,s,v=cv2.split(hsv_image)
cv2.imshow("H SPLIT",h)
cv2.imshow("S SPLIT",s)
cv2.imshow("V SPLIT",v)
MERGED_IMAGE=cv2.merge((h,s,v))
cv2.imshow("HSV MERGED IMAGE",MERGED_IMAGE)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### IMAGE 
# H SPLITED:
![Screenshot 2024-02-16 121302](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/5d46b267-4117-429d-b44c-9401d1738943)
# S SPLITED:
![Screenshot 2024-02-16 121248](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/c1593417-be1d-4466-a883-18efad8c591a)
# V SPLITTED:
![Screenshot 2024-02-16 121228](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/fa81a146-d66a-4154-9aea-2711fed744c7)
# IMAGE MERGED:
![Screenshot 2024-02-16 121209](https://github.com/Hariveeraprasad-2006/COLOR_CONVERSIONS_OF-IMAGE/assets/145049988/efb8b3f5-19bc-4815-9730-514886e97497)
## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







