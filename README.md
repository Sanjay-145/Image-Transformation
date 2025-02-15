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

# Program:
## Developed By: P.Sanjay
## Register Number: 212220230042
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
![translation](https://user-images.githubusercontent.com/75235426/165502121-cc74d9ce-5b15-4c39-9068-dc596b40bc0f.png)



### ii) Image Scaling

![scaling](https://user-images.githubusercontent.com/75235426/165502223-d89d5699-a418-4b09-821a-534bd8c2a5e4.png)



### iii)Image shearing
![shearing](https://user-images.githubusercontent.com/75235426/165502301-c04f62c9-f993-4dda-9052-2d5de5db9328.png)


### iv)Image Reflection
![reflection](https://user-images.githubusercontent.com/75235426/165502325-176c8c30-60f7-4a89-ac08-581bf30a2918.png)



### v)Image Rotation
![rotation](https://user-images.githubusercontent.com/75235426/165502334-271eeb80-d476-4b50-abf8-6c4a7ba449a7.png)


### vi)Image Cropping
![cropping](https://user-images.githubusercontent.com/75235426/165502352-3457aa84-18b2-4f93-ad15-0ca931bab538.png)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
