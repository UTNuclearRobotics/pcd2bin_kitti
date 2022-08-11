## PCD to KITTI binary converter

Convert .pcd pointcloud files into KITTI binary files.\
This is a fork of [LINK](https://github.com/leofansq/Tools_RosBag2KITTI/tree/master/pcd2bin). \
All credits go to the original author.

## Instructions

1. Clone this repository into your ros2 workspace's src folder
```
cd ~/ros2_ws/src
git clone https://github.com/nerovalerius/pcd2bin_kitti
```

Change the paths inside ``src/pcd2bin.cpp``` to the corresponding paths of your setup. 

e.g.:

```
std::string bin_path = "/home/user/dataset/pointclouds_binary/";
std::string pcd_path = "/home/user/dataset/pointclouds/";
```

Build the node:
```
cd ~/ros2_ws
colcon build
```

Source workspace and run the node:
```
source ~/ros2_ws/install/setup.bash
ros2 run pcd2bin_kitti pcd2bin
```