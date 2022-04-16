# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:

Import cv2 and save and image as filename.jpg
### Step2:

Use imread(filename, flags) to read the file.

### Step3:

Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:

Split and merge the image using cv2.split and cv2.merge commands.

### Step5:

End the program and close the output image windows.

## Program:
```python
# Developed By:Tamil Venthan RS
# Register Number:212220230054
import cv2
img=cv2.imread("rr.jpg")
cv2.imshow("trade",img)
cv2.waitKey(0)

# i) Convert BGR and RGB to HSV and GRAY
bgr_hsv = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',bgr_hsv)
bgr_gray = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',bgr_gray)
#rgb to hsv and gray
rgb_hsv = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',rgb_hsv)
rgb_gray = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',rgb_gray)
cv2.waitKey(0)




# ii)Convert HSV to RGB and BGR
hsv_rgb = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',hsv_rgb)
hsv_bgr = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',hsv_bgr)
cv2.waitKey(0)





# iii)Convert RGB and BGR to YCrCb
rgb_ycrcb = cv2.cvtColor(img,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',rgb_ycrcb)
bgr_ycrcb = cv2.cvtColor(img,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',bgr_ycrcb)
cv2.waitKey(0)



# iv)Split and Merge RGB Image
blue=img[:,:,0]
green=img[:,:,1]
red=img[:,:,2]
cv2.imshow("B",blue)
cv2.imshow("G",green)
cv2.imshow("R",red)
#merge rgb
Merge_rgb=cv2.merge((blue,green,red))
cv2.imshow("Merge_RGB",Merge_rgb)
cv2.waitKey(0)



# v) Split and merge HSV Image
h,s,v=cv2.split(bgr_hsv)
cv2.imshow("H",h)
cv2.imshow("S",s)
cv2.imshow("V",v)
#merge hsv
Merge_hsv=cv2.merge((h,s,v))
cv2.imshow("Merge_hsv",Merge_hsv)
cv2.waitKey(0)



```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>

![2022-04-16](https://user-images.githubusercontent.com/75235477/163673464-1b76e776-b56a-405c-b3a1-18a84cd9e9d5.png)


<br>

### ii) HSV to RGB and BGR
<br>

![2022-04-16 (2)](https://user-images.githubusercontent.com/75235477/163673475-c0b7514d-47ce-4fb7-bd67-df700102a8ac.png)

<br>

### iii) RGB and BGR to YCrCb
<br>

![2022-04-16 (3)](https://user-images.githubusercontent.com/75235477/163673481-4b37166f-304f-4488-acb9-11146e00edb4.png)

<br>

### iv) Split and merge RGB Image
<br>

![2022-04-16 (4)](https://user-images.githubusercontent.com/75235477/163673509-2584280d-9bb7-4e9a-8595-3791cf36fcdf.png)


<br>

### v) Split and merge HSV Image
<br>

![2022-04-16 (5)](https://user-images.githubusercontent.com/75235477/163673513-7350d82f-37bb-4357-aa91-dbb0b51aec86.png)


<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
