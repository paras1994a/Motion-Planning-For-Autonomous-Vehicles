# Motion-Planning-For-Autonomous-Vehicles

The Project involved Implementing a Behavoiur Planner and a Motion Planner for Automated Driving in Carla Simulation Environment. 
Car should be able to follow its Driving Lane, Safely Avoid static obsctacles on its way and Stop at Traffic Lights. 




![GIF-220516_194440](https://user-images.githubusercontent.com/56697957/168652247-3e923cd8-dec2-412b-9ecf-32a56f0b7105.gif)

### Behaviour Planning 
This module is supposed to take decisons about selecting an appropriate driving Maneuver based on the Car's immediate environment and actual driving Scenario in Simulation.
Possible Maneuvers ata any given time are : 
1. Follow Lane and drive at Cruise Speed 
2. Deaccelerating and Braking to Stop at Traffic Lights 
3. Remain Standstill until Traffic Light Turns Green.

### Motion Planning 
This Problem is sub divided into Path Planning and Velocity profile Generation.

1. Multiple Possible Paths between Car's current Position and Next Goal Point are computed by using Cubic Spirals.
2. Velocity Profiles are generated for these Spirals based on the type of Maneuver Selected by Behaviour Planner.
   These profiles are different for when Following Lane or Braking to stop at Traffic Light 

### Choosing Best Driving Trajectory

Cost is Computed for Every possible spiral Trajectory based on chances of collision and proximity to Centre of the driving lane.
Collisions are penalised while driving near Lane Centre line is rewarded. Minimum cost trajectory is selected.<br>





![project image](https://user-images.githubusercontent.com/56697957/168626486-f0eb86da-a522-4acf-9630-4db6e24c01d8.JPG)


### Installation and Dependencies 
The starter Project Code is provided by Udacity. git clone https://github.com/udacity/nd013-c5-planning-starter.git. Download all the dependencies mentioned there if you want to run this project on your system

1. Run Carla Simulator
2. cd nd013-c5-planning-starter/project
3 ./install-ubuntu.sh
4. cd starter_files/
5. cmake .
6. make
7. cd nd013-c5-planning-starter/project
8. ./run_main.sh

   SimulatorAPI is the Python Carla Client Script for Setting up and Controlling the simulation.

### Scope of Extension 
 #### Dynamic Collision Detection & Avoidance
 Incorporate Intent Predection algorithms in order to avoid collision with moving Actors/Obstacles in Simulation
 
 #### Planning Other Complex Driving Maneuvers
 Lane Changing
 Safely Following Vehicle in the front
 
 
