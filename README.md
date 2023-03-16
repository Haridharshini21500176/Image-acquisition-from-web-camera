# Image-Acquisition-from-Web-Camera
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Import cv2 and capture the video using cv2.VideoCapture(0)

### Step 2:
Write the captured image using cv2.imwrite("NewPicture.jpg",frame)

### Step 3:
Resize the image using cv2.resize(frame, (0,0), fx = 0.5, fy=0.5)

### Step 4:
Display the image until the loop gets over

### Step 5:
Rotate the image using cv2.rotate(smaller_frame,cv2.cv2.ROTATE_180)


### Developed By:Haridharshini.S
### Register No:212221230033

## Program:
## i) Write the frame as JPG file
```
VidCap = cv2.VideoCapture(0)
while(True):
    ret,frame = VidCap2.read()
    cv2.imshow('video_image',frame)
    cv2.imwrite("hari.jpg",frame)
    if cv2.waitKey(1) == ord('q'):
        break
    result = False
VidCap.release()
cv2.destroyAllWindows()

```

## ii) Display the video
```
VidCap=cv2.VideoCapture(0)
while(True):
    ret,frame=VidCap.read()
    cv2.imshow('myimage',frame)
    if cv2.waitKey(1) == ord('q'):
        break
VidCap.release()
cv2.destroyAllWindows()
```
## iii) Display the video by resizing the window
```
cap=cv2.VideoCapture(0)
while(True):
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame = cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2,:width//2]=smaller_frame
    image[height//2:,:width//2]=smaller_frame
    image[:height//2,width//2:]=smaller_frame
    image[height//2:,width//2:]=smaller_frame
    
    cv2.imshow('quadrant_screen',image)
    if cv2.waitKey(1) == ord('q'):
        break
VidCap.release()
cv2.destroyAllWindows()
````
## iv) Rotate and display the video
```
cap=cv2.VideoCapture(0)
while(True):
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame = cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2,:width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:,:width//2]=smaller_frame
    image[:height//2,width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:,width//2:]=smaller_frame
    
    cv2.imshow('quadrant_rotated_screen',image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image

![exp 2 a](https://user-images.githubusercontent.com/94168395/225538344-183d980d-5ff0-47b3-bbce-27e389a1c7bd.png)


### ii) Display the video

![exp 2b](https://user-images.githubusercontent.com/94168395/225538783-6b5c5bf4-4a33-40e5-86ad-d3b733e79cd0.jpeg)


### iii) Display the video by resizing the window

![exp 2c](https://user-images.githubusercontent.com/94168395/225538908-635af602-2bda-443b-b765-340207c2d1bb.jpeg)

### iv) Rotate and display the video

![exp 2d](https://user-images.githubusercontent.com/94168395/225539017-3aeb02f3-9cbc-4925-9354-45e230d99732.png)


## Result:
Thus the image is accessed from webcamera and displayed using openCV.
