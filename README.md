# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

### Step2:

Read the input image using cv2.imread() and store it in a variable for further processing.


### Step3:

Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

1.Translation moves the image along the x or y-axis.
2.Scaling resizes the image by scaling factors.
3.Shearing distorts the image along one axis.
4.Reflection flips the image horizontally or vertically.
5.Rotation rotates the image by a given angle.

### Step4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.

### Step5:
Save or display the final transformed images for analysis and use plt.show() to display them inline in Jupyter or compatible environments.

## Program:
<br> 

## Program:
```python
Developed By:PREM R
Register Number: 212223240124
i)Image Translation

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for correct display
plt.title("Original Image")  
plt.axis('off')
tx, ty = 100, 50  # Translation factors (shift by 100 pixels horizontally and 50 vertically)
M_translation = np.float32([[1, 0, tx], [0, 1, ty]])  # Translation matrix: 
# [1, 0, tx] - Horizontal shift by tx
# [0, 1, ty] - Vertical shift by ty
translated_image = cv2.warpAffine(image, M_translation, (image.shape[1], image.shape[0]))
plt.imshow(cv2.cvtColor(translated_image, cv2.COLOR_BGR2RGB))  # Display the translated image
plt.title("Translated Image")  
plt.axis('off') 


ii) Image Scaling

fx, fy = 5.0, 2.0  
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)
plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))  # Display the scaled image
plt.title("Scaled Image")  # Set title
plt.axis('off')



iii)Image shearing

shear_matrix = np.float32([[1, 0.5, 0], [0.5, 1, 0]])
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))
plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB))  # Display the sheared image
plt.title("Sheared Image")  # Set title
plt.axis('off')



iv)Image Reflection

reflected_image = cv2.flip(image, 2)
plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB))  # Display the reflected image
plt.title("Reflected Image")  # Set title
plt.axis('off')




v)Image Rotation

(height, width) = image.shape[:2] 
angle = 45
center = (width // 2, height // 2)
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)
rotated_image = cv2.warpAffine(image, M_rotation, (width, height))
plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB))  # Display the rotated image
plt.title("Rotated Image")  # Set title
plt.axis('off')




vi)Image Cropping

x, y, w, h = 100, 100, 200, 150  # Define the top-left corner (x, y) and the width (w) and height (h) of the crop
# Cropping the image from coordinates (x, y) to (x+w, y+h)
cropped_image = image[y:y+h, x:x+w]
plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB))  # Display the cropped image
plt.title("Cropped Image")  # Set title
plt.axis('off')





```
## Output:
## i)Original Image
![Screenshot 2025-03-25 092810](https://github.com/user-attachments/assets/24056fe3-aaaa-40b4-9909-10fb305a71a4)


### ii)Image Translation
![Screenshot 2025-03-25 092846](https://github.com/user-attachments/assets/1bc40a81-3b68-4d75-a6de-8867e5fbca8f)



### iii) Image Scaling
![Screenshot 2025-03-25 092916](https://github.com/user-attachments/assets/b8735b93-3ecd-4863-9304-49ab9c3e2776)



### iv)Image shearing
![Screenshot 2025-03-25 092942](https://github.com/user-attachments/assets/437a2240-d26b-404f-babd-d7cc87bb04c5)



### v)Image Reflection
![Screenshot 2025-03-25 093012](https://github.com/user-attachments/assets/7b504d36-1534-4fff-8581-e10e92f26389)




### vi)Image Rotation
![Screenshot 2025-03-25 093044](https://github.com/user-attachments/assets/7ae29f22-75ae-41b6-8fa8-184ab55e1b0e)




### vii)Image Cropping
![Screenshot 2025-03-25 093120](https://github.com/user-attachments/assets/44939c84-e823-41c4-8f13-8ab2540f4004)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
