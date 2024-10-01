# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:

### Developed By: Jeevanesh
### Register Number: 212222243002

### Colour and Gray Image:
```
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('Spb.jpeg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
```
# Load the color image
image = cv2.imread('SPB Dark.jpg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
### Histogram of Grayscale Image:
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

```

### Histogram Equalization of Grayscale Image:
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
## Output:

### Input Image
![image](https://github.com/user-attachments/assets/36834306-05f4-406f-82d9-52382cd90966)


### Histogram of Grayscale Image
![image](https://github.com/user-attachments/assets/17c98e96-9f07-4667-bcad-60c01cf46f55)


### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/4ea6d245-7dd1-4d29-9593-3eefed4c94ef)

![image](https://github.com/user-attachments/assets/aa0d3461-31a0-49eb-b271-d5b2bae407a9)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
