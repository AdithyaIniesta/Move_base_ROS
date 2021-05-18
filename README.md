### Move_base_ROS
### Problem Statement <br>
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
