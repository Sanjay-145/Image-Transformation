# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using

M=np.float32([[1,0,20],[0,1,50],[0,0,1]])

translated_img=cv2.warpPerspective(input_img,M,(cols,rows))


### Step3:
Scale the image using

M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]])

scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step4:
Shear the image using

M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]])

sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))


### Step5:
Reflection of image can be achieved through the code

M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])

reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))


### Step 6:
Rotate the image using

angle=np.radians(45)

M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])

rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))


### Step 7:
Crop the image using

cropped_img=input_img[20:150,60:230]


### Step 8:
Display all the Transformed images.

## Program:
### Developed By: P.Sanjay
### Register Number: 212220230042

### i)Image Translation
```
M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()
```
### ii) Image Scaling
```
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```
### iii)Image shearing
```
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```
### iv)Image Reflection
```
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```
### v)Image Rotation
```
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```
### vi)Image Cropping
```
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation

![translation](https://user-images.githubusercontent.com/75235426/166114219-337dae04-cb9c-4ab9-8413-751952b87671.png)

### ii) Image Scaling

![scaling](https://user-images.githubusercontent.com/75235426/166114228-b6fd41b1-0436-419f-aa70-43ca90fc7d17.jpeg)

### iii)Image shearing

![shearing](https://user-images.githubusercontent.com/75235426/166114274-f102d489-4dd7-492c-a0d7-4e8f7c2d0ec4.png)

### iv)Image Reflection

![reflection](https://user-images.githubusercontent.com/75235426/166114280-b9e73850-68ec-44a9-87ba-d54f6bb670e6.png)

### v)Image Rotation

![rotation](https://user-images.githubusercontent.com/75235426/166114382-a50f3eff-944a-44e6-b057-ec7b187ce33d.jpeg)

### vi)Image Cropping

![cropping](https://user-images.githubusercontent.com/75235426/166114389-ba835b97-c9b7-41fb-8f2e-2af4b6247931.jpeg)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
