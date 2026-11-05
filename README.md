# Geometric-Transformations-Using-OpenCV
04: Image Transformations Using OpenCV

## Aim

To write a Python program using OpenCV to perform various geometric transformations on an image, such as translation, scaling, shearing, reflection, rotation, and cropping.

## Software Used

- Python
- Jupyter Notebook
- OpenCV (`cv2`)
- NumPy
- Matplotlib

## Algorithm

### Step 1: Import Libraries
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2: Load the Image
Read the input image using `cv2.imread()` and display the original image.

### Step 3: Image Translation
- Create a translation matrix.
- Shift the image horizontally and vertically.
- Apply the transformation using `cv2.warpAffine()`.
- Display the translated image.

### Step 4: Image Scaling
- Define scaling factors for width and height.
- Resize the image using `cv2.resize()`.
- Apply bilinear interpolation using `cv2.INTER_LINEAR`.
- Display the scaled image.

### Step 5: Image Shearing
- Create a shearing transformation matrix.
- Apply horizontal and vertical shearing.
- Use `cv2.warpAffine()` to perform the transformation.
- Display the sheared image.

### Step 6: Image Reflection
- Perform image reflection using `cv2.flip()`.
- Apply flipping along both axes.
- Display the reflected image.

### Step 7: Image Rotation
- Calculate the center of the image.
- Create a rotation matrix using `cv2.getRotationMatrix2D()`.
- Rotate the image by 45 degrees.
- Apply the transformation using `cv2.warpAffine()`.
- Display the rotated image.

### Step 8: Image Cropping
- Specify the starting coordinates.
- Define the required width and height.
- Extract the required portion using NumPy array slicing.
- Display the cropped image.

## Program


## Program

**Developed By:** Santhose Arockiraj J

**Register Number:** 212224230248

**Program File:** `Ex.4(2).ipynb`

### Step 1: Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### Step 2: Load the Image

```python
# Step 1: Load the image
image = cv2.imread('my.jpeg')  # Load the image from file
```

### Step 3: Display the Original Image

```python
# Display the original image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for correct display
plt.title("Original Image")  
plt.axis('off') 
```

### Step 4: Image Translation

```python
# Step 2: Image Translation
tx, ty = 100, 50  # Translation factors (shift by 100 pixels horizontally and 50 vertically)
M_translation = np.float32([[1, 0, tx], [0, 1, ty]])  # Translation matrix: 
# [1, 0, tx] - Horizontal shift by tx
# [0, 1, ty] - Vertical shift by ty
translated_image = cv2.warpAffine(image, M_translation, (image.shape[1], image.shape[0]))  
```

```python
plt.imshow(cv2.cvtColor(translated_image, cv2.COLOR_BGR2RGB))  # Display the translated image
plt.title("Translated Image")  
plt.axis('off')
```

### Step 5: Image Scaling

```python
# Step 3: Image Scaling
fx, fy = 5.0, 2.0  # Scaling factors (1.5x scaling for both width and height)
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)
# resize: Resize the image by scaling factors fx, fy
# INTER_LINEAR: Uses bilinear interpolation for resizing
```

```python
plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))  # Display the scaled image
plt.title("Scaled Image")  # Set title
plt.axis('off')
```

### Step 6: Image Shearing

```python
# Step 4: Image Shearing
shear_matrix = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  # Shearing matrix
# The matrix shears the image by a factor of 0.5 in both x and y directions
# [1, 0.5, 0] - Shear along the x-axis (horizontal)
# [0.5, 1, 0] - Shear along the y-axis (vertical)
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))
```

```python
plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB))  # Display the sheared image
plt.title("Sheared Image")  # Set title
plt.axis('off')
```

### Step 7: Image Reflection

```python
# Step 5: Image Reflection
reflected_image = cv2.flip(image, 2)  # Flip the image horizontally (1 means horizontal flip)
# flip: 1 means horizontal flip, 0 would be vertical flip, -1 would flip both axes
```

```python
plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB))  # Display the reflected image
plt.title("Reflected Image")  # Set title
plt.axis('off')
```

### Step 8: Image Rotation

```python
# Step 6: Image Rotation
(height, width) = image.shape[:2]  # Get the image height and width
angle = 45  # Rotation angle in degrees (rotate by 45 degrees)
center = (width // 2, height // 2)  # Set the center of rotation to the image center
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)  # Get the rotation matrix
# getRotationMatrix2D: Takes the center of rotation, angle, and scale factor (1 means no scaling)
rotated_image = cv2.warpAffine(image, M_rotation, (width, height))  # Apply rotation
```

```python
plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB))  # Display the rotated image
plt.title("Rotated Image")  # Set title
plt.axis('off')
```

### Step 9: Image Cropping

```python
# Step 7: Image Cropping
x, y, w, h = 100, 100, 200, 150  # Define the top-left corner (x, y) and the width (w) and height (h) of the crop
# Cropping the image from coordinates (x, y) to (x+w, y+h)
cropped_image = image[y:y+h, x:x+w]
# The crop is performed by slicing the image array in the y and x directions
```

```python
plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB))  # Display the cropped image
plt.title("Cropped Image")  # Set title
plt.axis('off')
```


## Output

### 1. Original image 

- Original image is displayed.

<img width="230" height="323" alt="image" src="https://github.com/user-attachments/assets/7974fd22-e428-4af4-962a-b539a0a41138" />


### 2. Image Translation

- Translated image is displayed after shifting.

<img width="243" height="319" alt="image" src="https://github.com/user-attachments/assets/7229a1b5-8ec2-45d6-baa3-c1d6e17682f8" />


### 3. Image Scaling

- Scaled image is displayed with the specified scaling factors.

<img width="416" height="254" alt="image" src="https://github.com/user-attachments/assets/9403c09c-5a20-4d65-9f95-ef92f8f2712c" />


### 4. Image Shearing

- Horizontally and vertically sheared images are displayed.

<img width="243" height="325" alt="image" src="https://github.com/user-attachments/assets/43fa3149-f2dd-4439-b0c8-c8d2a29267e2" />


### 5. Image Reflection

- Reflected image is displayed after flipping along both axes.

<img width="244" height="329" alt="image" src="https://github.com/user-attachments/assets/4829fae8-400d-4944-8038-b7f5279f4ff9" />


### 6. Image Rotation

- Rotated image is displayed at an angle of 45 degrees.

<img width="245" height="327" alt="image" src="https://github.com/user-attachments/assets/a6f96f91-b28f-472c-8aee-66ac27efcdb6" />


### 7. Image Cropping
- Cropped portion of the image is displayed.

<img width="403" height="337" alt="image" src="https://github.com/user-attachments/assets/32c48718-fa94-4a29-8643-668ddfdccf97" />


## Result

Thus, various geometric transformations such as image translation, scaling, shearing, reflection, rotation, and cropping were successfully performed using OpenCV. These transformations demonstrate how images can be spatially manipulated for different computer vision applications.
