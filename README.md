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

Replace video_feed value with your value of the camera.
```
roslaunch usb_cam usb_cam-test.launch video_feed:="/dev/video2"
```

Replace markerId and markerSize with your values. Checkout more arguments inside the launchfile.
```
roslaunch aruco_bunkier aruco_marker_finder.launch markerID:=0 markerSize:=0.1
```

Run Rviz with config file.
```
rosrun rviz rviz -d src/aruco_detect/aruco.rviz
```

## Authors and sources
* **Krzysztof Stężała** - *Initial work* - [filesmuggler](https://github.com/filesmuggler)
* **usb_cam** - *Repo modification* - [usb_cam repository](https://github.com/ros-drivers/usb_cam)
