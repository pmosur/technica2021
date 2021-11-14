# technica2021
This Github hosts our Technica 2021 project: XD is a program which aims to mitigate harm from distracted driving. 

## Inspiration
Distracted driving is a widespread issue that has led to fatal injuries and deaths. Drivers are most commonly distracted by their phone, and texting while driving is very prevalent among young people. We were inspired by previous applications of machine learning to apply computer vision and machine learning to this scenario to help combat the issue of distracted driving.

## What it does
Our program uses computer vision and machine learning to identify whether a driver’s eyes have moved away from the road for a significant amount of time. The driver's eye movements are recorded by the camera that the driver faces, and once the driver has been found by our program to have looked away from the road for at least 7 seconds, an alert message will show on the screen and an alert sound will play, notifying the driver to focus. 

## How we built it
Our program was coded using python and libraries. We used dlib, a machine learning and computer vision facial recognition library, to identify facial features in a live webcam feed. We also used OpenCV, an open source computer vision and machine learning library, to create a threshold for the eye locations determined by the dlib network and segment out the center of the eyes using a midpoint method. Then, we used miniscule ratios to determine whether eye movement was significant enough to determine a lack of focus from the road. Our program played an alert sound and displayed an alert message once it found that significantly unfocused eye movement by the driver was present for at least 7 seconds.

## Challenges we ran into
One challenge we faced was detecting a visual threshold of looking down. Finding the right threshold was difficult to implement, especially while accounting for a rectangular webcam feed, since we had to experiment with ratios. Another challenge we faced was calculating how much time the driver was distracted for based on a live webcam feed. However, we were able to work around this issue through keeping a timer and resetting only in certain scenarios.

There was also a runtime lag that we could not fix because we used a computer webcam camera, as well as a slight delay in having the camera locate the driver's eyes and processing the direction the driver's eyes were looking. The lag could also be possibly due to the dim lighting in the area we tested our product in, or the specific processing speed of the camera. 

## Accomplishments that we're proud of
Our program was able to successfully detect eye movement, identify when eyes moved away from the webcam, and display visual and audio messages when they did for at least 7 seconds. Additionally, the program successfully timed how long eyes were away from the webcam for.

## What we learned
We learned about the dlib library and how it can help with facial feature recognition, as well as the playsound library to play a sound in our program. We gained more experience in using OpenCV and python.

## What's next for XD
In the future, we want to fix the runtime lag of our program by testing it in a location with more natural lighting and using a camera with a higher processing speed. Next, while we built this product to be compatible with a computer webcam, we would like to expand it to be compatible with a small camera that can be placed at eye level with the driver. 

Sources:
https://pysource.com/2019/01/04/eye-motion-tracking-opencv-with-python/
https://www.itprotoday.com/development-techniques-and-management/how-do-i-download-files-github
https://towardsdatascience.com/real-time-eye-tracking-using-opencv-and-dlib-b504ca724ac6
https://www.geeksforgeeks.org/play-sound-in-python/
https://towardsdatascience.com/distracted-driver-detection-using-deep-learning-e893715e02a4
https://realpython.com/python-timer/
https://www.studytonight.com/post/dlib-68-points-face-landmark-detection-with-opencv-and-python
