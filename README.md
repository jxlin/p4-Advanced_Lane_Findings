## Robust lane finding using advanced computer vision techniques: Mid project update
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

This repository is the code accompanying medium post [Robust lane finding using advanced computer vision techniques: Mid project update](https://medium.com/@vivek.yadav/robust-lane-finding-using-advanced-computer-vision-techniques-mid-project-update-540387e95ed3#.yra5pu3j6)


Lane finding is crucial for developing algorithms for autonomous driving robots or self-driving cars. The lane-finding algorithm must be robust to changing light conditions, weather conditions, other cars/vehicles on the road, curvature of road and type of road itself. In this post, we present an algorithm based on advanced computer vision techniques to identify left and right lanes from dash-mounted camera video. We implemented the lane finding algorithm in the following steps,

1. Undistort camera image and apply perspective transform to get a bird-eye view of the street.
2. Convert to HSV colorspace and apply color mask to identify yellow lines
3. Apply Sobel filters to get image with potential line/edges
4. Combine binary masks from Sobel filters and HSV color masks
5. Apply moving average filter to remove any markings or features that could be due to other artifacts in the image.
6. Apply polynomial regression to compute the left and right lanes
7. Apply frame to frame smoothing to discard noise between images, and draw lines back on the image.
8. Compute curvature and lane deviation and write them on the image.

All the steps above can be viewed in the youtube video below. 

[![Diagnostics for advanced lane finding using computer vision](https://img.youtube.com/vi/PJ8i0VY_pug/0.jpg)](https://www.youtube.com/watch?v=PJ8i0VY_pug)


List of files below,

1. main_undistort_camera.ipynb Ipython notebook to generate distortion parameters and camera matrix. 
2. camera_calibration.pkl pickle file with distortion parameters and camera matrix values, to be used in main_lane_markings_* files for undistorting camera image. 
3. main_lane_markings_22.ipynb Ipython notebook with code to analysis individual camera image
4. main_lane_markings_fin2.ipynb Ipython notebook with code to analyse the whole video. 
5. project_video.mp4, project_video_output.mp4 and project_video_output_diagnosis.mp4 project video, output video and diagnosis video of project video file. 

