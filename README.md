<img src="img/header.jpg" alt="Header" width="100%"/>

The repository is meant for leveraging system development and robot deployment for ground-based autonomous navigation and exploration on the NVIDIA Isaac-sim. Containing autonomous navigation modules such as collision avoidance, terrain traversability analysis, waypoint following, etc, and a set of visualization tools. This repository use the hospital environment and carter robot from the Isaac example files, see [here](https://docs.omniverse.nvidia.com/app_isaacsim/app_isaacsim/install_basic.html#isaac-sim-first-run) for Isaac-sim environment installation and Nucleus server setup.

## Quick Start 

The repository has been tested in Ubuntu 18.04 with [Ros Melodic](http://wiki.ros.org/melodic/Installation) and Ubuntu 20.04 with [ROS Noetic](http://wiki.ros.org/noetic/Installation). Install dependencies with command lines below.

```sudo apt update```

```sudo apt install libusb-dev```

Clone the open-source repository.

```git clone https://github.com/JingtianYan/autonomous_exploration_development_environment_isaac_sim.git```

In a terminal, go to the folder and compile.

```cd autonomous_exploration_development_environment_isaac_sim```

```catkin_make```

Source the ROS workspace and launch the system.

```source devel/setup.sh```

```roslaunch isaac_simulator system_isaac.launch```

## Running the NVIDIA Isaac-Sim

Hardware Requirement: Isaac-Sim requires **NVIDIA RTX GPU** with **470+ GPU driver** version. 

This repository use Isaac-Sim environment for development. Download and Install the NVIDIA Isaac-Sim simulator environment from the [official guide](https://docs.omniverse.nvidia.com/app_isaacsim/app_isaacsim/install_basic.html#isaac-sim-first-run). Also, our development enviroment depend on some example environment from the Nvidia. Thus, install and set up Nucleus server follow the instructions from [offical guide](https://docs.omniverse.nvidia.com/prod_nucleus/prod_nucleus.html).

Then, running the simulation and load the robot into the Isaac-Sim. 

```~/.local/share/ov/pkg/isaac_sim-2021.2.1/python.sh ./src/isaac_simulator/isaac_env/isaac_hospital_env.py```

Replace "~/.local/share/ov/pkg/isaac_sim-2021.2.1" with your installation path if you changed it.

## TARE planner

The result is available [here](https://www.youtube.com/watch?v=Kpt596Q3FoU)

For using TARE planner using this development environment. After running the simulator and Isaac-sim, please follow instructions [here](https://github.com/caochao39/tare_planner) to run.


## FAR planner

The result is available [here](https://www.youtube.com/watch?v=WxP7fuE4zdQ)

For using FAR planner using this development environment. After running the simulator and Isaac-sim, please follow instructions [here](https://github.com/MichaelFYang/far_planner) to run.
