# Super_lio

## 改进
在ros2分支下

增加了world->base_link的tf变化
增加了odom_base的odom 描述base_link的位置

base_link表示机器人的frame 以及位置

***注：原代码的lio.extrinsic.odom_robo 好像odom的变换有问题，但是tf变换正常***

## 待改进

增加base_link相关变换的固定[x,y,z,yaw,pitch,roll]于yaml
现在的是代码内的硬编码
src/ros/ROSWrapper.cpp pub_odom 649行  
                     imuHandler 382行

```bash
sudo apt install libgoogle-glog-dev libtbb-dev
```

## run

```bash
source install/setup.bash
ros2 launch super_lio Livox_mid360.py
```