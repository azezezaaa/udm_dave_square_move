# udm_dave_square_move
This repo contains Part 3 of CFDL labs in MIAR on using a Turtlebot3 WafflePi for mapping and navigation. In this repo, the turtlebot3 is made to draw a square in rviz. Note that this part is run in simulation and not directly on the turtlebot3. 

## Step 1
### Ensure the following packages are installed. Note that not all of them are required.
```
$ cd ~/catkin_ws/src
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_applications.git
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_applications_msgs.git
$ cd .. && catkin_make
$ source devel/setup.bash
```
## Step 2
### Download and install the git repo.
```
$ cd ~/catkin_ws/src
$ git clone https://github.com/azezezaaa/udm_dave_square_move.git
$ cd ~/catkin_ws/
$ catkin_make && source devel/setup.bash
$ export TURTLEBOT3_MODEL=waffle_pi
```
## Step 3
### Terminal A
```
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
### Terminal B
Note that map.yaml and map.pgm must be placed in $HOME directory.
```
$ roslaunch udm_dave_square_move turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```
### Terminal C
```
$ rosrun udm_dave_square_move movebase_square.py
```
