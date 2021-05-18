### 
### Move_base_ROS: Problem Statement <br>
- Implement a python script to guide a mobile robot to different goal poses. 
- Print the total time taken to visit goal poses. 
- The mobile robot should return to initial pose when the program is interrupted by Ctrl + C. 

### Instructions  

```
cd (path to catkin workspace)/src
git clone https://github.com/AdithyaIniesta/Move_base_ROS.git
cd ..
catkin build
source ~/.bashrc
Terminal 1: echo "export MAP_NAME="neo_workshop"" >> ~/.bashrc
source ~/.bashrc

Source all the terminals
Terminal 1: roslaunch neo_simulation simulation.launch 
Terminal 2: roslaunch neo_simulation mpo_700_amcl.launch 
Terminal 3: roslaunch neo_simulation mpo_700_move_base.launch 
Terminal 4: roslaunch adithya_navigate adithya_bringup.launch
```

### Demo and Results
#### Screenshot of Gazebo world and RViz map is taken from the official repository of Neobotix GmbH [1]
1. Green arrows indicate different goal poses with respect to map co-ordinate system. 
![RVIZ2](https://user-images.githubusercontent.com/13369817/118699743-2e430b80-b812-11eb-8406-245ebaea0be0.png)
2. The red arrow indicates the pose of the robot and the goal reach is confirmed when the red arrow of the robot aligns with the green arrow. 
![RVIZ3](https://user-images.githubusercontent.com/13369817/118699813-461a8f80-b812-11eb-89d0-70ce083647fc.png)
3. If the node is interrupted or if all the goal poses are visited, the robot will return to the initial pose. 
![Screenshot from 2021-05-18 13-17-46](https://user-images.githubusercontent.com/13369817/118700280-c93be580-b812-11eb-8533-bd12f1c097b9.png)
4. Sample output when all three goal poses are visited by the robot. 
  - Total time to reach 3 goals:= 57.54 seconds
5. When Ctrl + C is pressed, traversal to next goal and remaining goal poses are terminated and the robot will return back to initial pose. In this case, the program will report collective time taken to visit all the visited goals. For example:
  - Total time to reach 2 goals:= 38.11 seconds
### Reference Repositories
- [1] https://github.com/neobotix/neo_simulation
- [2] http://edu.gaitech.hk/turtlebot/map-navigation.html
