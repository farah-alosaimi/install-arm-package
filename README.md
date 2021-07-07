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
## 2- Installing the package arduino_robot_arm



### 3-Controlling the motors
~~~python
roslaunch robot_arm_pkg check_motors.launch
~~~
### arm is ready
