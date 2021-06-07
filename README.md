# Project-Description
This is a course project of SDM5002 in SUSTech. We want to build a fire firefighting robot, which can follow the designed route and detect the early fire and smoke, then extinguish it.

# Project Name
Ceasefire

# Prerequisites

We test the library and the code in AMD64 Ubuntu 18.04, but it should be run in other architecture platforms, such as the Nvidia Jeston series platforms.

Following is the libraies this project needs:
- ROS: https://www.ros.org
- OpenCV: https://opencv.org
- Ceres: http://www.ceres-solver.org
- ROS Package for Realsense camera: https://github.com/IntelRealSense/realsense-ros
- ROS Package for Tracer Mobile Base: https://github.com/agilexrobotics/tracer_ros
- ROS Package for YOLOv3: https://github.com/leggedrobotics/darknet_ros
- ROS web video server: https://github.com/RobotWebTools/web_video_server
- ROS WebSocket server: https://github.com/RobotWebTools/rosbridge_suite
- node.js and npm: https://nodejs.org/en/download/

# Install


Install and run the gimbal control module

```bash
cd catkin/src
git clone https://github.com/Movable-Fire-Alarm-System/Gimbal-Control.git
cd ..
catkin_make
rosrun gimbal_control gimbal_control
```

Install and run the vehicle control module

```bash
cd catkin/src
git clone https://github.com/Movable-Fire-Alarm-System/Visual-Inspection-Robot.git
cd ..
catkin_make
rosrun Visual_Inspection_Robot Visual_Inspection_Robot
```

Install and run the web management system
```bash
git clone https://github.com/Movable-Fire-Alarm-System/web_interface.git
npm install express
node test.js
```

Run the Realsense camera 
```bash
roslaunch realsense2_camera rs_camera.launch
```

Run the ros web video server
```bash
rosrun web_video_server web_video_server
```

Run the ros WebSocket server
```bash
roslaunch rosbridge_server rosbridge_websocket.launch
```

Run YOLOv3 fire detector
```bash
roslaunch darknet_ros darknet_ros.launch
```

Open your web browser and access: http://0.0.0.0:8000

# Share link
Onedrive link: https://1drv.ms/u/s!AglpiexMFEKDg6kaVzyggCsJw6YdGQ?e=LFYswX
