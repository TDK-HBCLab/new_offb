# new_offb
The package has to use usb_cam package that optimize the camera using some about linux kit, then send image using ros msg through cv_bridge package. So I made a node that is responsible for receiving a image messages(required cv_bridge), for the purpose of image processing using OpenCV.

Installation (The following steps type your terminal) :

Requirement : First, you have to install ROS distro(I use kinetic distro), this is their official websit : http://www.ros.org/. Second, you have to prepare a camera compatible your computer.

$mkdir -p ~/your_workspace/src

$cd your_workspace

$catkin_make

$cd src

$git clone https://github.com/TDK-HBCLab/new_offb.git

$git clone https://github.com/ros-drivers/usb_cam.git

$cd ..

$catkin_make

$source ~/your_workspace/devel/setup.bash

$roslaunch usb_cam usb_cam-test.launch

$source ~/your_workspace/devel/setup.bash                     
(Open a new terminal) or offboard computer, but you have to modify your .bashrc file changing your ROS_MASTER_URI before you do this statement. And source your .bashrc file($ source ~/.bashrc).

$rosrun new_offb Image



