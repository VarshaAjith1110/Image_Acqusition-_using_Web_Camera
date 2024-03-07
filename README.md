# Image_Acqusition-_using_Web_Camera
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
### Step 1:Use cv2.VideoCapture(0) to access web camera
<br>

### Step 2:Use cv2.imread to read the video or image
<br>

### Step 3:Use cv2.imread to read the video or image
<br>

### Step 4:Use cv2.imshow to show the video
<br>

### Step 5:End the program and close the output video window by pressing 'q'.
<br>

## Program:
``` Python
### Developed By:VARSHA AJITH
### Register No:212221230118

## i) Write the frame as JPG file

import cv2
videoCaptureObject = cv2.VideoCapture(0)

while (True):
    ret,frame = videoCaptureObject.read()
    cv2.imwrite("NewPicture.jpg",frame)
    
    result = False
videoCaptureObject.release()
cv2.DestroyAllWindows()


## ii) Display the video

import cv2
videoCaptureObject = cv2.VideoCapture(0)

while(True):
    ret,frame = videoCaptureObject.read()
    cv2.imshow('myimage',frame)
    if cv2.waitKey(1) == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()





## iii) Display the video by resizing the window


import cv2
import numpy as np
cap  = cv2.VideoCapture(0)
while True:
    ret,frame = cap.read()
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8)
    small_frame = cv2.resize(frame,(0,0),fx =0.5, fy = 0.5)
    image[:height//2, :width//2]=small_frame
    image[height//2:, :width//2]=small_frame
    image[:height//2, width//2:]=small_frame
    image[height//2:, width//2:]=small_frame
    cv2.imshow('myimage',image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()



## iv) Rotate and display the video



import cv2
import numpy as np
cap  = cv2.VideoCapture(0)
while True:
    ret,frame = cap.read()
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8)
    small_frame = cv2.resize(frame,(0,0),fx =0.5, fy = 0.5)
    image[:height//2, :width//2]=cv2.rotate(small_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=small_frame
    image[:height//2, width//2:]=small_frame
    image[height//2:, width//2:]=cv2.rotate(small_frame,cv2.ROTATE_180)
    cv2.imshow('myimage',image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()






## Output

### i) Write the frame as JPG image
</br>
![WhatsApp Image 2024-03-07 at 08 28 57_9098702b](https://github.com/VarshaAjith1110/Image_Acqusition-_using_Web_Camera/assets/94222288/5de2ac89-c4db-4035-9828-81cad7eb3879)

</br>


### ii) Display the video

![WhatsApp Image 2024-03-07 at 08 29 15_ad1e9a92](https://github.com/VarshaAjith1110/Image_Acqusition-_using_Web_Camera/assets/94222288/dedf5f38-e942-4e66-85a3-e652041b78c2)




### iii) Display the video by resizing the window

![WhatsApp Image 2024-03-07 at 08 29 05_e9e078bc](https://github.com/VarshaAjith1110/Image_Acqusition-_using_Web_Camera/assets/94222288/946d7c0d-1da1-47d3-9f6f-7eb0cdab0a34)





### iv) Rotate and display the video

![WhatsApp Image 2024-03-07 at 08 29 26_61d16c0e](https://github.com/VarshaAjith1110/Image_Acqusition-_using_Web_Camera/assets/94222288/f7bff1d2-bbe6-4b2b-946f-27c9920a4642)






## Result:
Thus the image is accessed from webcamera and displayed using openCV.
