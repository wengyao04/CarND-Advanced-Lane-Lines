## Advanced Lane Finding
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

### Calibrate Camera
Apply `cv2.findChessboardCorners()` on [chessboard images](https://github.com/wengyao04/CarND-Advanced-Lane-Lines/tree/master/camera_cal) to identify corners as `imgpoints`, and save the corners of a horizontal chessbaord (size=9x5) in a 3D array `objpoints`.  `cv2.calibrateCamera()` is used to calculate the distortion coefficients and calibration matrix. The following images show the chessboard without/with calibration.

<img src="./output_images/calibrate_chess.jpg" width="600"/>

### Gradient Threshold
Pass gray scaled image to the cv2.Sobel() taht takes the derivative of the image in x or y direction. Taking the gradient in the x direction emphasizes edges closer to vertical. Alternatively, taking the gradient in the y direction emphasizes edges closer to horizontal. I try different thresholds to detect the lane lines

| absolute sobel  | magnitude of sobel | direction of sobel | combined color threshold |
|:----------------:|:------------------:|:------------------:|:------------------:|
| absolute sobel_x |  sqrt(sobel_x*sobel_x + sobel_y*sobel_y) | arctan(sobel_y/sobel_x) | s-channel of HLS and absolute sobel_x |

<img src="./output_images/test_images_threshold.jpg" width="800"/>

### Perspective Transform
<img src="./output_images/test_images_warp.jpg" width="850"/>

<img src="./output_images/test_images_fit.jpg" width="850"/>

<img src="./output_images/test_images_fit_region.jpg" width="800"/>


<img src="project_output.gif" width="800"/>
