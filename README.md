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

### 1. Image Translation
- Original image is displayed.
- Translated image is displayed after shifting.

### 2. Image Scaling
- Original image is displayed.
- Scaled image is displayed with the specified scaling factors.

### 3. Image Shearing
- Original image is displayed.
- Horizontally and vertically sheared images are displayed.

### 4. Image Reflection
- Original image is displayed.
- Reflected image is displayed after flipping along both axes.

### 5. Image Rotation
- Original image is displayed.
- Rotated image is displayed at an angle of 45 degrees.

### 6. Image Cropping
- Original image is displayed.
- Cropped portion of the image is displayed.

## Result

Thus, various geometric transformations such as image translation, scaling, shearing, reflection, rotation, and cropping were successfully performed using OpenCV. These transformations demonstrate how images can be spatially manipulated for different computer vision applications.
