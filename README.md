#colored_pointcloud package
- 下载及安装：
在工作空间中的src打开终端，输入
```
git clone https://github.com/WuShuang73/colored_pointcloud
cd ..
catkin_make
```
- 准备工作：
首先要标定相机内参以及相机和雷达的外参，将内参矩阵(intrinsic matrix)、失真系数(distortion coefficients)以及外参矩阵(extrinsic matrix)写入 config路径下的calib_result.yaml文件中。

接着修改launch/colored_pointcloud_node161.launch文件中相机和雷达的topic

播放标定数据包
```
rosbag play test.bag -l
```
最后运行
```
source devel/setup.bash
roslaunch colored_pointcloud colored_pointcloud161.launch 
```
