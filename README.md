
# Multi-agent Trajectory Optimization

## Description
We have focused on understanding the novel trajectory planning technique proposed in the reference paper- "Efficient trajectory planning for multiple non-holonomic mobile robots via prioritized trajectory optimization". Further, we have analyzed and discussed the methodology of the solution. The simulation results are replicated and the significant inferences stated by the authors are validated. Finally, the hyper-parameters of the solution are altered to extract additional inferences.

## 1. Software Requirements
* Ubuntu 20.04
* ROS Noetic
* Octomap
* Ipopt

## 2. Installation instructions
#### - Install Ipopt solver
Follow [Ipopt Installation](https://coin-or.github.io/Ipopt/INSTALL.html).

#### - Install dependencies
```
sudo apt-get install ros-noetic-octomap*
sudo apt-get install ros-noetic-dynamic-edt-3d
sudo apt-get install cppad
```
#### - Build:
Copy the folder `files/multi_agent_opt_traj` and paste it in the src folder of your catkin workspace. The following commands can then be run to build the package.
```
cd <catkin_ws> && catkin_make
source ~/catkin_ws/devel/setup.bash
```
## 3. Run Simulations
#### Warehouse
```
roslaunch multi_robot_traj_planner prioritized_plan_warehouse.launch 
```

#### Environment with random obstacles
```
roslaunch multi_robot_traj_planner prioritized_plan_random_env.launch
```

## 4. Results
1. Video recordings from our experiment are in the `output/videos` folder.
2. Adaptation results can be viewed in the `output/inferences_*` folders.


## Simulation Data
Data gathered from the simulations can be viewed in the `simulation_data` folder.

## 4. Acknowledgments
Our implementation is built on top of the work of the official repo of the reference paper[Efficient trajectory planning for multiple non-holonomic mobile robots via prioritized trajectory optimization](https://github.com/LIJUNCHENG001/multi_robot_traj_planner) 
