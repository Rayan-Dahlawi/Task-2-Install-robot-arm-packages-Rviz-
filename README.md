# Task 2 Robotics and AI
### Install robot arm packages (Rviz)



In task 2, we will install robot arm packages (Rviz) on Ubuntu Linux operating system on the terminal.

******

These are the commands of the installation that should be written on the Linux terminal (Noetic version):


```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
```
sudo apt install curl
```
```
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```
```
sudo apt-get update
```
```
sudo apt-get install ros-noetic-desktop-full
```
```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
```
```
source ~/.bashrc
```
```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```
```
sudo apt install python3-rosdep
```
```
sudo rosdep init
```
```
rosdep update
```
```
mkdir -p ~/catkin_ws/src
```
```
cd ~/catkin_ws/
```
```

catkin_make
```
```
cd ~/catkin_ws/src
```
```
git clone https://github.com/smart-methods/arduino_robot_arm.git 
```
```
cd ~/catkin_ws
```
```
rosdep install --from-paths src --ignore-src -r -y
```
```
sudo apt-get install ros-noetic-moveit
```
```
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
```
```
sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
```
```
sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```
```
catkin_make
```
```
roslaunch robot_arm_pkg check_motors.launch
```
```
sudo nano ~/.bashrc
```
At the end of the (bashrc) file add the follwing line
(source /home/wesam/catkin_ws/devel/setup.bash)
But !!! we just change (wesam) on the path to my name (Rayan).
then 
ctrl + o

```
source ~/.bashrc
```
To lunch Rviz :
```
roslaunch robot_arm_pkg check_motors.launch
```
