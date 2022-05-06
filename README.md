# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.<br>

Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.<br>

Step3:
Display the histograms with their respective images.<br>

Step4:
Equalize the grayscale image.<br>

Step5:
Display the grayscale image.<br>

## Program:
```python
# Developed By:G Venkata Pavan Kumar.
# Register Number: 212221240013
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

gray_image=cv2.imread('dog.jpg')
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.imshow(gray_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()



# Display the histogram of gray scale image and any one channel histogram from color image


color_image=cv2.imread('bike.jpg')
hist=cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.imshow(color_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('colorscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show(


# Write the code to perform histogram equalization of the image. 

gray_image = cv2.imread('car1.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()





```
## Output:
### Input Grayscale Image and Color Image
![42 1](https://user-images.githubusercontent.com/94827772/167061262-459e915d-0b47-4204-b4b3-fd3d363cb878.png)
![dip41](https://user-images.githubusercontent.com/94827772/167061267-f434e9ec-7907-4b93-a137-e99125e016f3.png)

### Histogram of Grayscale Image and any channel of Color Image
![dip41 2](https://user-images.githubusercontent.com/94827772/167061353-1d6baeab-d0e9-4813-adb8-4e51dc7fcb2c.png)
![dip42 2](https://user-images.githubusercontent.com/94827772/167061356-6655bae2-9f20-4c06-a1e8-366fcb90d821.png)


### Histogram Equalization of Grayscale Image
![dip43](https://user-images.githubusercontent.com/94827772/167061400-701070fa-a830-4e0d-b38a-fbe1fd7fd2ea.png)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
