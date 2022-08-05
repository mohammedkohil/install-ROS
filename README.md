# install-ROS
Robot Operating System: Installation Instructions for Ubuntu

Setup Ubuntu in a VM
1- Get a free key for VMware Fusion Player
2- On the same page, download VMware Fusion player for your operating System
3- Install VMware Fusion Player
4-Get the Ubuntu 20.04 ISO
5-Install Ubuntu as a VMware virtual machine

Setup ROS
On your Ubuntu machine, follow these steps to install ROS Noetic:
Add the ROS package repository to your sources.list, and import the required keys.
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
For maximum compatibility of your system with the tutorials and other systems, make a Desktop Full Install of ROS
sudo apt update && sudo apt install ros-noetic-desktop-full
Install additional packages:
sudo apt install liburdfdom-tools ros-noetic-robot-state-publishe


Starting ROS
When all packages are installed, it's time to test the installation.

Run the following command to export additional path variables in your shell, so that you can execute all the ROS binaries
source /opt/ros/noetic/setup.bash
Start a demo of the simulation tool gazebo
roslaunch walker_gazebo walker.launch
If you see the GUI application starting - like in the following picture - your installation is complete.
Now permanently add the new new env vars to your shell with
echo '`source /opt/ros/noetic/setup.bash`' > ~/.bashrc
