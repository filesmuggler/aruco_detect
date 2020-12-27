# aruco_detect
Repo for aruco tag detection

## Initial setup 

```
git clone https://github.com/filesmuggler/aruco_detect

```

## Camera calibration

If your Camera_Info topic returns empty K,P,D matrices (all zeros), you sould calibrate your camera first. 
Follow the tutorial on [website](http://wiki.ros.org/camera_calibration/Tutorials/MonocularCalibration).

You will obtain ost.yaml file which is the calibration file to feed to the node running camera.

You should copy this file to the calibration folder in usb_cam in your workspace.

## Running detection

