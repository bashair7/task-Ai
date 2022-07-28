# task2-Ai

# arduino_robot_arm

**These packages were tested under ROS kinetic and Ubuntu 20.04 and it works perfectly on ROS  noetic**

# Dependencies

***run this instruction inside your workspace:***

```  

$ rosdep install --from-paths src --ignore-src -r -y  
```

***for noetic distro***

``` $ sudo apt-get install ros-noetic-moveit
$ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
$ sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control 
```

# Robot Arm

# Circuit diagram



# Robot initial positions



# Configuring Arduino with ROS

Install Arduino IDE in Ubuntu[https://www.arduino.cc/en/software]
open the terminal in Arduino IDE
install run 

```$ sudo ./install.sh 
```

Install the arduino package and ros library[http://wiki.ros.org/rosserial_arduino/Tutorials/Arduino%20IDE%20Setup]

install rosserial for Arduino

``` 
sudo apt-get install ros-indigo-rosserial-arduino

sudo apt-get install ros-indigo-rosserial

```

# Install ros_lib into the Arduino Environment

```cd <sketchbook>/libraries
  rm -rf ros_lib
  rosrun rosserial_arduino make_libraries.py .
  ```

# Finishing Up

***After restarting your IDE, you should see ros_lib listed under examples:***




***Make sure to change the port permission before uploading the Arduinocode 
```
$ sudo chmod 777 /dev/ttyUSB0
```

# 1- USAGE

# Controlling the robot arm by joint_state_publisher in the terminal 


```
$ roslaunch robot_arm_pkg 

check_motors.launch
```

# 2- Controlling the robot arm by Moveit and kinematics

```
$ roslaunch moveit_pkg demo.launch
```


