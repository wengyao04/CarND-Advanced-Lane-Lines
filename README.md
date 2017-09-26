## Advanced Lane Finding
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

### Calibrate Camera
Apply `cv2.findChessboardCorners()` on [chessboard images](https://github.com/wengyao04/CarND-Advanced-Lane-Lines/tree/master/camera_cal) to identify corners and save them as `imgpoints`. `objpoints` is a 3D array and stores the corners of a horizontal chessbaord with a size of 9x5.  `cv2.calibrateCamera()` is used to calculate the distortion coefficients and calibration matrix. Following images show the chessboard without/with calibration.

<img src="./output_images/calibrate_chess.jpg" width="600"/>

### Gradient Threshold
<img src="./output_images/test_images_threshold.jpg" width="800"/>

<img src="./output_images/test_images_warp.jpg" width="850"/>

<img src="./output_images/test_images_fit.jpg" width="850"/>

<img src="./output_images/test_images_fit_region.jpg" width="800"/>


<img src="project_output.gif" width="800"/>
