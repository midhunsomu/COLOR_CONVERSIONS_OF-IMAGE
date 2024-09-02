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
        resized_img[i][j] = 1  # Set the pixel to white
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
cv2.imshow('212223240087', resized_img)
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
## i) Read and display the image

![1](https://github.com/user-attachments/assets/add525e4-e425-47fc-b6a0-8d2843ca4580)

## ii)Write the image

![10](https://github.com/user-attachments/assets/233e92d7-3743-49a9-9cd0-cf6af958a324)


## iii)Shape of the Image

![2](https://github.com/user-attachments/assets/7f91a0c0-c0c2-4ea7-91bc-8ee21c23dc6e)


## iv)Access rows and columns and cut portion of image

![3](https://github.com/user-attachments/assets/d9d37f88-0763-4015-bbf1-dd82435d7a20)


## v)Paste portion of image

![4](https://github.com/user-attachments/assets/1a6deeb7-9ae0-4a9c-b7eb-d378fe972977)

## vi) BGR and RGB to HSV and GRAY

![5](https://github.com/user-attachments/assets/1c040764-1584-44c4-8414-169f6c3f166c)


## vii) HSV to RGB and BGR

![6](https://github.com/user-attachments/assets/cca06fb6-dacf-4620-ab2e-70e8912bc752)


## viii) RGB and BGR to YCrCb

![7](https://github.com/user-attachments/assets/e505c646-d03e-4154-b902-99f02e7909b7)


## ix) Split and merge RGB Image

![8](https://github.com/user-attachments/assets/b9ffd8fa-5142-4cda-9daa-1f65d825b6b1)


## x) Split and merge HSV Image

![9](https://github.com/user-attachments/assets/28ab34fe-2b11-4280-9259-5877229bea6d)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
