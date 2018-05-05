![Screenshot](/capture.bmp)
Sample map built from [nsh_indoor_outdoor.bag](http://www.frc.ri.cmu.edu/~jizhang03/Datasets/nsh_indoor_outdoor.bag) (opened with [ccViewer](http://www.danielgm.net/cc/))

:white_check_mark: Tested with ROS Indigo and Velodyne VLP16. [(Screencast)](https://youtu.be/o1cLXY-Es54)

All sources were taken from [ROS documentation](http://docs.ros.org/indigo/api/loam_velodyne/html/files.html)

Ask questions [here](https://github.com/laboshinl/loam_velodyne/issues/3).

How to build with catkin:

```
$ cd ~/catkin_ws/src/
$ git clone https://github.com/laboshinl/loam_velodyne.git
$ cd ~/catkin_ws
$ catkin_make -DCMAKE_BUILD_TYPE=Release 
$ source ~/catkin_ws/devel/setup.bash
```

Running:
```
roslaunch loam_velodyne loam_velodyne.launch
```
## Results
***Husky Dataset***

<a href="https://drive.google.com/file/d/1Snvz9VU2-CtfGEVY1_JzVO7b-XaeRaFL/view?usp=sharing">video link</a>

<img src="imgs/husky.png" width="712pix" />

***Quad Dataset***

<a href="https://drive.google.com/file/d/1dji3F1K1WyiPXrWMNWNLNFjQwYLJgAue/view?usp=sharing">video link</a>

<img src="imgs/quad.png" width="712pix" />


## Husky Dataset Instructions
Download [husky.bag](https://drive.google.com/file/d/1QqVY7z-3ojrfrI3Q6LTY4Ui_0nkOpEqO/view?usp=sharing) into catkin_ws/bags/

```bash
roslaunch hdl_graph_slam husky.launch
rosrun hdl_graph_slam bag_player.py bags/husky.bag
```

## Quad Dataset Instructions
Download [nardos3.bag](https://drive.google.com/file/d/1jjilcRgPEUWECLCSd0r0EZuduAeX_RGM/view?usp=sharing) into catkin_ws/bags/

## Requirements
*Note that this package should be installed in ROS indigo in Ubuntu 14.04*


In second terminal play sample velodyne data from [VLP16 rosbag](https://db.tt/t2r39mjZ):
```
rosbag play ~/Downloads/velodyne.bag 
```

Or read from velodyne [VLP16 sample pcap](https://midas3.kitware.com/midas/folder/12979):
```
roslaunch velodyne_pointcloud VLP16_points.launch pcap:="/home/laboshinl/Downloads/velodyne.pcap"
```

---
[Quantifying Aerial LiDAR Accuracy of LOAM for Civil Engineering Applications.](https://ceen.et.byu.edu/sites/default/files/snrprojects/wolfe_derek.pdf) Derek Anthony Wolfe

[ROS & Loam_velodyne](https://ishiguro440.wordpress.com/2016/04/05/%E5%82%99%E5%BF%98%E9%8C%B2%E3%80%80ros-loam_velodyne/) 
