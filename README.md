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

**Developed By:** Santhose Arockiraj J

**Register Number:** 212224230248

**Program File:** `Ex.4.ipynb`

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
