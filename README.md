![Screenshot](/husky_map.bmp)
Sample map of NSH B floor built from [husky.bag]

## Requirements
*Note that this package should be installed in ROS indigo in Ubuntu 14.04*

The following ROS packages are required:
- pcl_ros
- <a href="https://github.com/laboshinl/loam_velodyne.git">loam_velodyne</a>
```bash
sudo apt-get install ros-indigo-pcl-ros

```

How to build loam_velodyne with catkin:
```bash
$ cd ~/catkin_ws/src/
$ git clone https://github.com/laboshinl/loam_velodyne.git
$ cd ~/catkin_ws
$ catkin_make -DCMAKE_BUILD_TYPE=Release 
$ source ~/catkin_ws/devel/setup.bash

```
## Husky Dataset Instructions
Download [husky.bag](https://drive.google.com/file/d/1QqVY7z-3ojrfrI3Q6LTY4Ui_0nkOpEqO/view?usp=sharing)

## Quad Dataset Instructions
Download [nardos3.bag](https://drive.google.com/file/d/1jjilcRgPEUWECLCSd0r0EZuduAeX_RGM/view?usp=sharing)

## Running
```
roslaunch loam_velodyne loam_velodyne.launch
```
In second terminal play sample husky or quadcopter velodyne data:
```
rosbag play ~/Downloads/husky.bag
              (or)
rosbag play ~/Downloads/nardo3.bag
```
---
