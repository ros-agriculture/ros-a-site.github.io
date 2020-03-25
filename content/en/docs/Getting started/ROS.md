---
title: "ROS"
linkTitle: "ROS"
date: 2017-01-05
description: >
 An introduction to ROS
 
---

# Learning ROS
 * [ROS Tutorials on http://wiki.ros.org](http://wiki.ros.org/ROS/Tutorials)
 * [Johns Hopkins University - ROS Short Course](https://dscl.lcsr.jhu.edu/home/courses/ros_short_course_fall_2017/)
 * [The Construct - Robot Ignite Acadamy](https://www.robotigniteacademy.com)

# ROS Documentation
* [ROS Wiki](http://wiki.ros.org)
* [Coordinate Frames for Mobile Platforms](http://www.ros.org/reps/rep-0105.html)

# ROS Software
You can download a prebuilt image for a raspberry pi or vitural machine here: [Ubiquity Robotics Download](https://downloads.ubiquityrobotics.com/)

If you would like to install ROS on your Ubuntu machine we use the install script from [Linorobot](https://github.com/linorobot/rosme).

# Questions
* [Get answers to ROS questions on http://answers.ros.org](http://answers.ros.org)
* [What frame is sensor_msgs::Imu.orientation relative to?](https://answers.ros.org/question/50870/what-frame-is-sensor_msgsimuorientation-relative-to/)

# AWS RoboMaker

* [RoboMaker Documentation](https://docs.aws.amazon.com/robomaker/latest/dg/what-is-robomaker.html)
* [RoboMaker Cheeat Sheet](https://www.techrepublic.com/article/aws-robomaker-a-cheat-sheet/)
* [Deep Racer](https://github.com/aws-robotics/aws-robomaker-sample-application-deepracer)
* [Colcon Bundle Format](https://github.com/colcon/colcon-bundle/blob/master/BUNDLE_FORMAT.md)

## Build and bundle ROS1 projects locally using colcon

In this example, we will build and bundle the hello world simulation workspace from AWS RoboMaker:

* Clone the repository in your local machine: 

`git clone https://github.com/aws-robotics/aws-robomaker-sample-application-helloworld.git`

* Run ros-kinetic-colcon docker image: 

`docker run -it -v $(pwd):/workspace nubonetics/ros-kinetic-colcon /bin/bash`

* In the docker image, go to the workspace folder: 

`cd aws-robomaker-sample-application-helloworld/simulation_ws`

* Run the following commands to update and install dependencies:

`apt-get update`

`rosdep update`

`rosws update`

`rosdep install --from-paths src --ignore-src -r -y`

* Build the workspace:

`colcon build`

* Bundle the workspace:

`source install/local_setup.sh`

`colcon bundle --bundle-version 1`
