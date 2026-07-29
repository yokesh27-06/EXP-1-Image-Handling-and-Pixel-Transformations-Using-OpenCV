# EX-01 Image-Handling-and-Pixel-Transformations-Using-OpenCV 

## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

### Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.  
Display the original, brighter, and darker images.

### Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).  
Display the original, lower contrast, and higher contrast images.

### Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
- **Name:** YOKESH H
- **Register Number:** 212224230312

  ### Ex. No. 01

### **Step 1: Read and Display Image**
```python
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('vr46.png', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb, cmap='viridis')  
plt.title("Original Image")
plt.axis('off')  
plt.show()
```
### **Step 2: Draw a Line**
```python
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```

### **Step 3: Draw a Circle**
```python
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```

### **Step 4: Draw a Rectangle**
```python
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

### **Step 5: Add Text**
```python
text_img = cv2.putText(img_rgb, "Yokesh", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```

### **Step 6: Convert RGB to HSV**
```python
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```
### **Step 7: Convert RGB to Gray**
```python
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```
### **Step 8: Convert RGB to YCrCb**
```python
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```

### **Step 9: Convert HSV back to RGB**
```python
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```

### **Step 10: Modify Pixel Block**
```python
image[200:500, 200:500] = [255, 255, 255]
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```

### **Step 11: Resize Image**
```python
resized_image = cv2.resize(image, (768 // 2, 600 // 2))
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```

### **Step 12: Crop ROI**
```python
roi = image[50:350, 50:350]
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```

### **Step 13: Flip Horizontally**
```python
image = cv2.imread('vr46.png')
flipped_horizontally = cv2.flip(image, 1)
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```

### **Step 14: Flip Vertically**
```python
flipped_vertically = cv2.flip(image, 0)
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```

### **Step 15: Save Final Image**
```python
cv2.imwrite(
"final_output.jpg",
flipped_horizontally
)**
```

## Output:
### Original Image
<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/22c95533-833f-45c2-9c84-84dd545d845e" />



### Image with Line
<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/46beaba6-1e7c-4bd0-b5e3-acab78f27bf8" />


### Image with Circle

<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/2026a3f2-beda-4a73-a902-740d05492ca1" />


### Image with Rectangle

<img width="552" height="395" alt="download" src="https://github.com/user-attachments/assets/eb8fed7a-9aaa-4909-80ff-b8d5c626e408" />

### Image with Text

<img width="552" height="395" alt="download" src="https://github.com/user-attachments/assets/56fbc186-3b64-4fb0-b498-5a637607d6a2" />


### HSV Images

<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/69d39a4d-f618-406b-b34f-3378726886a0" />
### Grayscale Images

<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/85609053-6a71-4fc5-8cd7-95424176e0b6" />
### YCrCb Images

<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/af80fe64-a46c-45a3-9d01-41a9179eb78d" />




### Resized Image

<img width="845" height="587" alt="image" src="https://github.com/user-attachments/assets/94953085-96d5-4020-9111-ba93168ff0d7" />


### Cropped ROI

<img width="377" height="381" alt="image" src="https://github.com/user-attachments/assets/84ce15af-6669-46b4-995a-d64dbf814e06" />

### Flipped Images

<img width="1328" height="880" alt="image" src="https://github.com/user-attachments/assets/e39f827c-6822-4450-8672-1c810baaf2ad" />


<img width="1312" height="887" alt="image" src="https://github.com/user-attachments/assets/abb8e088-29e9-4524-8ab4-24d3298d82a8" />


## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.

