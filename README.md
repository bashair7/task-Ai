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


![Screenshot 2022-07-29 035335](https://user-images.githubusercontent.com/81494917/181661503-6211cd08-7254-4dcb-8099-e675adc10a21.jpg)

# Robot initial positions

![Screenshot 2022-07-29 035356](https://user-images.githubusercontent.com/81494917/181660956-32579b5e-7328-4836-b9b1-f53fcfed855f.jpg)


# Configuring Arduino with ROS

Install Arduino IDE in Ubuntu[https://www.arduino.cc/en/software]
open the terminal in Arduino IDE
install run 

```
$ sudo ./install.sh 
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


![ss](https://user-images.githubusercontent.com/81494917/181661706-4893fccb-e09b-4882-96a5-9b1ea9ba2409.jpg)


***Make sure to change the port permission before uploading the Arduinocode***
```
$ sudo chmod 777 /dev/ttyUSB0
```

# 1- USAGE

# Controlling the robot arm by joint_state_publisher in the terminal 


```
$ roslaunch robot_arm_pkg check_motors.launch
```
***Result Run***

![USAGE ARDOUNO 1jpg](https://user-images.githubusercontent.com/81494917/181661092-460d257f-05ae-410e-a5cb-04881f3892d9.jpg)


# 2- Controlling the robot arm by Moveit and kinematics

```
$ roslaunch moveit_pkg demo.launch
```
***Result Run***

![Uploading ARDUNOARM.2jpg.jpg…]()
