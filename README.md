# arm-package-installing
## 1-prepare ros
### workspace
* alosaimi
~~~python
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
~~~
## 2-Install arduino_robot_arm package



## 3-motors Control
~~~python
roslaunch robot_arm_pkg check_motors.launch
~~~
## 4-arm is ready
