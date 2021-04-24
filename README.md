# Differential Drive robot
A Simple Differential Drive robot model, with gazebo differential drive plugin implemented.
This robot can be controlled by publishing twist messages to '/cmd_vel' topic.

## installation & running
1. Create a folder to hold workspace `$ mkdir -p ~/ws_diffdrive/src`
2. Create a new workspace by `$ cd ~/ws_diffdrive/src && catkin_init_workspace`
3. Compile the workspace `$ cd .. && catkin_make`
4. Source the workspace `$ echo "source ~/ws_diffdrive/devel/setup.bash" >> ~/.bashrc && source ~/.bashrc`

5. Clone the repo here `$ cd ./src/ && git clone link .`
6. Compile the workspace `$ cd ../ && catkin_make`
7. Launch the simulation `$ roslaunch diffdrive_description spawn_robot.launch`

8. To send command to '/cmd_vel' topic, `$ rostopic pub /cmd_v <tab><tab><tab>`, use tab autocomplete to get a template, edit values, press enter to send commands.

### Some Other tips
To get links and joints names (to update in gazebo plugin)
1. first convert xacro to urdf by `xacro diffdrive_robot.urdf.xacro > temp.urdf`
2. convert to pdf by `urdf_to_graphiz temp.urdf`
3. check structure here, make changes if necessary
