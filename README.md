# BlueRov-ROS-playground
Scripts to help BlueRov integration with ROS.
What is possible ?
- Video streaming capture with opencv
- Read and write over mavlink protocol with MAVROS
- Joystick interaction
- Gazebo simulation

<p align="center">
  <img src="doc/imgs/bluerov2_gazebo_underwater.png">
</p>


### Requirements
- [freebuoyancy_gazebo](https://github.com/youssefattia98/freebuoyancy_gazebo.git)



### Setup

````
cd 
nano .bashrc
export GAZEBO_MODEL_PATH=~{path to ardupilot_gazebo}/bluerov_ros_playground/model:$GAZEBO_MODEL_PATH
export GAZEBO_RESOURCE_PATH=~{path to ardupilot_gazebo}/bluerov_ros_playground/worlds:${GAZEBO_RESOURCE_PATH}
````

### Run with STIL

For BlueROV:

````
sim_vehicle.py -v ArduSub -L RATBeach -f gazebo-bluerov2 --out=udp:0.0.0.0:14550 --out=udp:127.0.0.1:14551 --console
gazebo worlds/underwater.world #for BlueROV

````

For BlueROV with heavy config:
````
sim_vehicle.py -v ArduSub -L RATBeach -f gazebo-bluerov2 --out=udp:0.0.0.0:14550 --out=udp:127.0.0.1:14551 --console
gazebo worlds/underwater_heavy_config.world 

````
