# Collision-avoidance-system-in-carla-v-0.9.5
This is a reinforcement learning project based on Carla simulator version 0.9.5
These python scripts are built on Carla simulator python API, therefore must be run from within the folder
Note this is still under development using reinforcement learning
Requirements
For the code RL_Adonia.py its is based on 
Tensorflow 1.13.1 
Keras 2.2.4, tensorflow is a backend library used in this project
It trains for 100 epochs and the tensorflow graghs are visualized showing the max, min and average rewards as the system learns.
The collision reward is given a very large negative value and no collision is rewarded 1.0.
If the agent(car) is initialized to move at a speed less than 50km/h.

For the code Adonia5.py it is based on tensorflow 2.0 and keras 2.3.0, for version compatibility issues, when running the code the tensorflow v2 is disabled and version 2 of tensorflow that is compatible with version 1 of tensorflow is enabled

Other packages that should be installed//
Numpy
pillow
future
matplotlib
opencv
