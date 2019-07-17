# ros_python3_ws

1. Clone the repo
2. Initialize a catkin workspace using ```catkin init```
3. Configure catkin build to use python3. Point to your version of Python 3 on your system - 
```
catkin config -DPYTHON_EXECUTABLE=/usr/bin/python3 -DPYTHON_INCLUDE_DIR=/usr/include/python3.5m  -DPYTHON_LIBRARY=/usr/lib/x86_64-linux-gnu/libpython3.5m.so
```
4. download packages:
```sudo apt install python3-pip```
```pip3 install numpy```   
```pip3 install empy```
```pip3 install pyyaml```
5. Build using ```catking build```
6. To use these packages, add this to your python path - ```${WORKSPACE_ROOT}/ros_python3_ws/install/lib/python3/dist-packages```
