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
### Step 1:
<br>
Import cv2 and capture the viedo using cv2.ViedoCapture(0).

### Step 2:
<br>
Write the capture image using cv2.imwrite("Kanishka.jpg",frame).

### Step 3:
<br>
Resize the image using cv2.resize(frame,(0,0),fx=0.5,fy=0.5).

### Step 4:
<br>
Display the image until the loop gets over.

### Step 5:
<br>
Rotate the image using cv2.rotate(smaller_frame,cv2.ROTATE_180).

## Program:
``` Python
### Developed By: Kanishka V S
### Register No: 212222230061
```
## i) Write the frame as JPG file
```
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("Kanishka.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```


## ii) Display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('212222230061_Kanishka',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```



## iii) Display the video by resizing the window
```



import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230061_Kanishka',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```




## iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230061_Kanishka',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()





```
## Output

### i) Write the frame as JPG image

![op1 dip](https://github.com/kanishka2305/Image_Acqusition-_using_Web_Camera/assets/113497357/04b3a196-7e37-4690-9b5a-830fb6c953ce)



### ii) Display the video
</br>
</br>

![op 2 dip](https://github.com/kanishka2305/Image_Acqusition-_using_Web_Camera/assets/113497357/a23fba8c-fc54-4697-8222-9263f905517d)


### iii) Display the video by resizing the window
</br>
</br>

![op3 dip](https://github.com/kanishka2305/Image_Acqusition-_using_Web_Camera/assets/113497357/b814bee6-1b61-4ec9-9b15-5765e29c946e)



### iv) Rotate and display the video
</br>
</br>

![op4 dip](https://github.com/kanishka2305/Image_Acqusition-_using_Web_Camera/assets/113497357/56867cc9-1da2-4438-81aa-8b7db7cd3a1c)




## Result:
Thus the image is accessed from webcamera and displayed using openCV.
