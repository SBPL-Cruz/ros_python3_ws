# ros_python3_ws

1. Clone the repo
2. Initialize a catkin workspace using ```catkin init```
3. Configure catkin build to use python3. Point to your version of Python 3 on your system - 
```
catkin config -DPYTHON_EXECUTABLE=/usr/bin/python3 -DPYTHON_INCLUDE_DIR=/usr/include/python3.5m  -DPYTHON_LIBRARY=/usr/lib/x86_64-linux-gnu/libpython3.5m.so
```
For using custom environment :
```
conda create --prefix ./py3_ros python=3.6 
catkin config -DPYTHON_EXECUTABLE=/media/yupeng/Data/ros_ws/py3_ros/bin/python -DPYTHON_INCLUDE_DIR=/media/yupeng/Data/ros_ws/py3_ros/include/  -DPYTHON_LIBRARY=/media/yupeng/Data/ros_ws/py3_ros/lib/libpython3.6m.so
```
* Install python3.6 dev following instructions [here](https://docs.python-guide.org/starting/install3/linux/). After this you need python include folder to cpp include - ``` export CPLUS_INCLUDE_PATH="$CPLUS_INCLUDE_PATH:/usr/include/python3.6m/```
* Install bullet - ```sudo apt-get install libbullet-dev``` for tf2_bullet
* You might have to add C++ support for vision_opencv [package](https://answers.ros.org/question/216842/ros-using-c-11-how-to-use-with-catkin/)

4. download packages:
```sudo apt install python3-pip```
```pip3 install numpy```   
```pip3 install empy```
```pip3 install pyyaml```
```pip3 install rospkg```
5. mkdir install
6. Build using ```catkin build```
7. To use these packages, add this to your python path - ```${WORKSPACE_ROOT}/ros_python3_ws/install/lib/python3/dist-packages```
