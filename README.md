# Go1_gazebo_simulation



## installation:

- clone the repo into the src folder of your local catkin_ws, e.g.:
```
cd ~/catkin_ws/src
git clone <url of this git repo>
```
- install dependacies using rosdep:
```
cd ~/catkin_ws
rosdep install --from-paths src --ignore-src -r -y
```
- build the ROS packages:
```
catkin build
```
- source the packages:
```
source ~/catkin_ws/devel/setup.bash
```
- (optional) add the source command to .bashrc for auto sourcing:
```
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
```


## Running the simulation
### Running the sim with navigation stack:

- start the gazebo simulation:
```
roslaunch go1_config gazebo.launch
```
- in a seperate terminal start the ROS navigation stack for the go1:
```
roslaunch go1_config navigate.launch rviz:=true
```