# IncreasingFPSwith-threading
Threading is very oftenly used to handle I/O heavy tasks such as reading frames from a camera sensor. 


In this repository, we will practice improving our FPS by creating a new thead that simply polls the camera for new frames while the main thread handles processing the current frame. 


In general, we will only be introducing one thread.

Main: process current frame
Thread 1: Tells camera to get new frame


The secret to getting a higher FPS with OpenCV is to move the I/O to a separate thread. (Bottleneck: reading of frame from camera sensor.)

ie. VideoCapture and .read() are both blocking operation. 
Main thread will be blocked until frame is read from camera and return to our script

Camera I/O are huge bottleneck as well after the computer vision and video processing

