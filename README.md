# Advanced Lane Finding
![Identifying Lanes](readme-resources/output.gif)

## [Udacity Self Driving Car Nanodegree: Computer Visison Project](https://in.udacity.com/course/self-driving-car-engineer-nanodegree--nd013/)


The goal of this project was to identify driving lanes in videos using computer vision techniques. Here is a summary of the how the code works:

* Camera calibration matrix and distortion coefficients are obtained from included calibration chessboard images.
* Raw image is undistorted using the matrix and coeefiicients obtained in the calibration step.
* A combination of Sobel transforms and thresholding in HSV colorspace is used to higlight lane edges in the image.
* The perspective of the transformed image is changed to top view or bird's eye view.
* Pixels beonging to lanes are identified using sliding window search.
* Curvature of the road is estimated from the identified lane pixels.
* A polynomial is fitted to the lane pixels.
* Lanes are plotted on top of the top view of the image using the polynomial fitted above.
* An inverse transform is performed, so the plotted lanes and curvagture information transfer back to the original image.
* In case of a video all the steps above are repeated or every frame.

The images for camera calibration are stored in the folder called `camera_cal`.  The images in `test_images` are for testing your pipeline on single frames.  If you want to extract more test images from the videos, you can simply use an image writing method like `cv2.imwrite()`, i.e., you can read the video in frame by frame as usual, and for frames you want to save for later you can write to an image file.  

To help the reviewer examine your work, please save examples of the output from each stage of your pipeline in the folder called `ouput_images`, and include a description in your writeup for the project of what each image shows.    The video called `project_video.mp4` is the video your pipeline should work well on.  

The `challenge_video.mp4` video is an extra (and optional) challenge for you if you want to test your pipeline under somewhat trickier conditions.  The `harder_challenge.mp4` video is another optional challenge and is brutal!

If you're feeling ambitious (again, totally optional though), don't stop there!  We encourage you to go out and take video of your own, calibrate your camera and show us how you would implement this project from scratch!
