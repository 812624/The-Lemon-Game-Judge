# The-Lemon-Game-Judge
This project is based on the famous game called "The Lemon in the Spoon Race" in which we need to hold the spoon straight in order to keep the lemon from falling off. Detect and track the lemon on the spoon.

## Algorithm Used

Project implements following algorithm:-

- Get the video.
- Divide the video into frames and for each frame do step 3-10.
- Convert each frame from BGR to HSV.
- Mask those objects in the HSV image which are in HSV threshold defined.
- Remove noise surrounding the object tracked by morphological algorithm called opening.
- Remove noise within the object tracked using closing.
- Retrieve number of pixels from finally masked image(img_mask3), whose value if non-zero then we have lemon color object in the frame, else lemon has fallen.
- Get the contours from the frame.
- Find the largest contour in the mask, then use it to compute the minimum enclosing circle and centroid.
- Display the circle and it's centre on the video frame.
- Close all windows.

## Dependencies:-

- Python
- Opencv
- numpy
