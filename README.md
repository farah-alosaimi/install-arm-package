# arm-package-installing
## 1-prepare ros
* workspace
~~~python
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
~~~
## 2-Install arduino_robot_arm package
* Add the “arduino_robot_arm” package to “src” folder
~~~python
cd ~/catkin_ws/src
sudo apt install git
git clone https://github.com/smart-methods/arduino_robot_arm 
~~~
* install all the dependencies
~~~python
cd ~/catkin_ws
rosdep install --from-paths src --ignore-src -r -y
sudo apt-get install ros-melodic-moveit
sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
~~~
* Compile the package
~~~python
catkin_make
~~~
## 3-motors Control
~~~python
roslaunch robot_arm_pkg check_motors.launch
~~~
## 4-arm is ready
