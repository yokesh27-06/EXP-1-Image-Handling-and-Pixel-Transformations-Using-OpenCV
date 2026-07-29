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

### **Step 1: # Display the image using Matplotlib**
```python
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```
### **Step 2: Image with Line**
```python
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2)   
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```

### **Step 3: Image with Circle**
```python
circle_img = cv2.circle(img_rgb,(550,300),150,(255,0,0),10)  
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('oN')  
plt.show()
```

### **Step 4: Image with Rectangle**
```python
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (1020, 690), (0, 0, 255), 10)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

### **Step 5: Image with text**
```python
text_img = cv2.putText(img_rgb, "Yokesh", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```
### **Step 6: Original RGB Image**



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

### HSV to RGB Image
<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/f3d045d3-5ee2-42f5-a0b5-3f76d39751b0" />

### Image with 300*300 White Block

<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/14c87925-a841-4e84-8ff4-ebf80d71ec0d" />



### Resized Image

<img width="493" height="409" alt="download" src="https://github.com/user-attachments/assets/a6a4670c-811c-4be4-905a-8b0cd7830c92" />


### Cropped ROI

<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/b731af8f-bc6b-4ee6-8c57-25e83bdc45f3" />

### Flipped Images

<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/e99bea5d-961b-483a-939b-27a77fd0b47c" />


<img width="515" height="371" alt="download" src="https://github.com/user-attachments/assets/c32faf82-c46a-4a07-9311-b487ddf92028" />


## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.

