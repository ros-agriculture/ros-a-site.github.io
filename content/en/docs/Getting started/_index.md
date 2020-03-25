
---
title: "ROS Agricuture User Guide"
linkTitle: "Getting Started"
weight: 3
date: 2019-03-01
description: >
  This page describes how to use the ROS Agriculture projects.
resources:
- src: "**spruce*.jpg"
  params:
    byline: "Photo: Bjørn Erik Pedersen / CC-BY-SA"
---

# [ros_lawn_tractor](https://github.com/ros-agriculture/ros_lawn_tractor)

[![lawn tractor image](http://img.youtube.com/vi/-RF8hOKg6WU/0.jpg)](https://www.youtube.com/watch?v=-RF8hOKg6WU)

## Install
If you don't have a Ubuntu computer running ROS. This [script](https://github.com/linorobot/rosme) provided by [LinoRobot](https://linorobot.org/) will install ROS for you.

<pre>
prompt$ cd catkin_ws/src
prompt/catkin_ws/src$ git clone https://github.com/ros-agriculture/ros_lawn_tractor.git 
prompt/catkin_ws/src$ git clone https://github.com/bsb808/geonav_transform.git
prompt/catkin_ws/src$ cd ..
prompt/catkin_ws$ rosdep update
prompt/catkin_ws$ rosdep install -y --from-paths . --ignore-src --rosdistro ${ROS_DISTRO}
prompt/catkin_ws$ sudo apt-get install python-catkin-tools
prompt/catkin_ws$ catkin build
prompt/catkin_ws$ source devel/setup.bash
prompt/catkin_ws$ roslaunch lawn_tractor_sim lawn_tractor_sim.launch
</pre>

## Docker
If you have docker installed skip to Download Start File. Otherwise, follow the [Docker installation instructions](https://docs.docker.com/install/).

### Download Start File
<pre>
prompt$ wget https://raw.githubusercontent.com/ros-agriculture/ros_lawn_tractor/master/docker/start.sh
prompt$ chmod +x start.sh
prompt$ ./start.sh
</pre>
..... wait for image to download ......
<pre>
docker/prompt$ roslaunch lawn_tractor_sim lawn_tractor_sim.launch
</pre>

When rviz starts it doesn't load the rviz config file.  You will need to go to File and load sim config file.
Sometimes when you press the File tab it just shows black.  You will need to stop rviz and relaunch the sim ([video](https://youtu.be/yF0pPZHdhtI))

## Licensing
ros_lawn_tractor is released under the MIT license. 

Any user of this software shall indemnify and hold harmless ROS Agriculture O&Uuml;. and its directors, officers, employees, agents, stockholders, affiliates, subcontractors and customers from and against all allegations, claims, actions, suits, demands, damages, liabilities, obligations, losses, settlements, judgments, costs and expenses (including without limitation attorneys’ fees and costs) which arise out of, relate to or result from any use of this software by user.

THIS IS ALPHA QUALITY SOFTWARE FOR RESEARCH PURPOSES ONLY. THIS IS NOT A PRODUCT. YOU ARE RESPONSIBLE FOR COMPLYING WITH LOCAL LAWS AND REGULATIONS. NO WARRANTY EXPRESSED OR IMPLIED.
