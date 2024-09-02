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
### Developed By: MIDHUN S
### Register Number: 212223240087


## Output:

### i) Read and display the image
```python3
import cv2
img = cv2.imread('MIDHUN S.jpg', 0)
resized_img = cv2.resize(img, None, fx=1, fy=1)
cv2.imshow('212223240087', resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### ii)Write the image
```python3
import cv2
img=cv2.imread('MIDHUN S.jpg',0)
cv2.imwrite('writed_walt.png',img)
```

### iii)Shape of the Image
```python
import cv2
img=cv2.imread('MIDHUN S.jpg',0)
print(img.shape)
```

### iv)Access rows and columns and cut portion of image
```python3
import cv2
img = cv2.imread('MIDHUN S.jpg', 0)
resized_img = cv2.resize(img, None, fx=1, fy=1)
for i in range(20, 100):
    for j in range(10, 50):
        resized_img[i][j] = 255  # Set the pixel to white
cv2.imshow('212223240087', resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### v)Paste portion of image
```python3
import cv2
img = cv2.imread('MIDHUN S.jpg', 0)
resized_img = cv2.resize(img, None, fx=1, fy=1)
copied_portion = resized_img[50:100, 100:150]
resized_img[4:54, 100:150] = copied_portion
cv2.imshow('212223240010', resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### vi) BGR and RGB to HSV and GRAY
```python3
import cv2
img = cv2.imread('MIDHUN S.jpg')
hsv_img = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
gray_img = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
cv2.imshow('Original Image', img)
cv2.imshow('HSV Image', hsv_img)
cv2.imshow('Grayscale Image', gray_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### vii) HSV to RGB and BGR
```python3
import cv2
img = cv2.imread('MIDHUN S.jpg')
hsv_img = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
rgb_img = cv2.cvtColor(hsv_img, cv2.COLOR_HSV2RGB)
bgr_img = cv2.cvtColor(hsv_img, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV Image', hsv_img)
cv2.imshow('RGB Image', rgb_img)
cv2.imshow('BGR Image', bgr_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### viii) RGB and BGR to YCrCb
```python3
import cv2
img = cv2.imread('MIDHUN S.jpg')
ycrcb_img = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('Original Image', img)
cv2.imshow('YCrCb Image', ycrcb_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### ix) Split and merge RGB Image
```python3
import cv2
img = cv2.imread('MIDHUN S.jpg')
b, g, r = cv2.split(img)
merged_img = cv2.merge((b, g, r))
cv2.imshow('Original Image', img)
cv2.imshow('Merged Image', merged_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### x) Split and merge HSV Image
```python3
import cv2
img = cv2.imread('MIDHUN S.jpg')
hsv_img = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv_img)
merged_hsv_img = cv2.merge((h, s, v))
merged_bgr_img = cv2.cvtColor(merged_hsv_img, cv2.COLOR_HSV2BGR)
cv2.imshow('Original Image', img)
cv2.imshow('Merged HSV Image', merged_bgr_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
i) Read and display the image

![DIP1](https://github.com/anu-varshini11/COLOR_CONVERSIONS_OF-IMAGE/assets/138969827/f051f44f-03da-4127-b049-8d4f9e6d8705)

ii)Write the image

![DIP2](https://github.com/anu-varshini11/COLOR_CONVERSIONS_OF-IMAGE/assets/138969827/83e02cc4-125c-4792-9d62-d41c5111e2d4)

iii)Shape of the Image

![DIP3](https://github.com/anu-varshini11/COLOR_CONVERSIONS_OF-IMAGE/assets/138969827/97df64c6-94a9-40cf-8924-8fdadeb2eaa7)

iv)Access rows and columns and cut portion of image

![DIP4](https://github.com/anu-varshini11/COLOR_CONVERSIONS_OF-IMAGE/assets/138969827/24ae6417-1e2c-4545-8c52-c80682510341)

v)Paste portion of image

![DIP5](https://github.com/anu-varshini11/COLOR_CONVERSIONS_OF-IMAGE/assets/138969827/32b1dda9-b21a-4a7c-88c8-c3e7a9e99a2c)

vi) BGR and RGB to HSV and GRAY

![DIP6](https://github.com/anu-varshini11/COLOR_CONVERSIONS_OF-IMAGE/assets/138969827/a81ae75d-3f5b-45c4-b51c-7e3322fd606b)

vii) HSV to RGB and BGR

![DIP7](https://github.com/anu-varshini11/COLOR_CONVERSIONS_OF-IMAGE/assets/138969827/a2328b9a-0480-4f20-bb7b-4282bd7ec5fc)

viii) RGB and BGR to YCrCb

![DIP8](https://github.com/anu-varshini11/COLOR_CONVERSIONS_OF-IMAGE/assets/138969827/67fed05a-5cac-4702-afe8-a4873f8dbff2)

ix) Split and merge RGB Image

![DIP9](https://github.com/anu-varshini11/COLOR_CONVERSIONS_OF-IMAGE/assets/138969827/15f866a7-b45a-4b12-b29d-8d65052bba41)

x) Split and merge HSV Image

![DIP10](https://github.com/anu-varshini11/COLOR_CONVERSIONS_OF-IMAGE/assets/138969827/53f1f5ae-d41e-4e19-9318-a8b1b6dfcaaf)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
