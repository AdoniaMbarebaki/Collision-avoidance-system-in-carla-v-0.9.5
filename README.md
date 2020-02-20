
# Project Title

Implementation of a Machine learning based forward collision avoidance system for vehicles using Reinforcement Learning

## Getting Started
This is a reinforcement learning project based on Carla simulator version 0.9.5. These python scripts are built on Carla simulator python API, therefore must be run from within the folder.
Note, this is still under development using reinforcement learning

### Prerequisites
For the above project to be up and running, the following dependencies must be satisfied.
CARLA_0.9.5 Simulator available on http://carla.org/2019/04/03/release-0.9.5/
Python 3.7.X, all versions above 3.7
Anaconda IDE python 3.7
```
Tensorflow 1.13.1 # for cpu and for gpu install tensorflow-gpu
```
Keras 2.2.4
pillow
opencv 

### What things you need to install the software and how to install them
Carla simulator version 0.9.5 requires a laptop of atleast 8GB RAM, and dedictated graphics of AMD or NVIDIA preferrably NVIDIA
After downloading and installing the simulator, add the folder to the environment path in the environment path variables
Downlaod Anaconda 3 with python 3.7 at https://www.anaconda.com/distribution/


### Installing
Downloading and installing the simulator when extracted has a PythonAPI folder that has supporting files like manual_control.py.
Carla simulator by default uses ports 2000, 2001 and 2002
For Carla manaual go to https://carla.readthedocs.io/en/latest/
Launch the simulator by running CarlaUE4.exe script from command prompt specifying the folder path where it is located.

```
pip install opencv
```
```
pip install pygame
```
```
pip install numpy
```
```
pip install tensorflow == 1.13.1 #for a specific version of tensorflow if required
```
```
pip install keras ==2.2.4 # for a specific version of keras if required
```

A step by step series of examples that tell you how to get a development env running

```
create an environment in anaconda
conda create -n collision_avoidance python 3.7
```

```
~path/CarlaUE4.exe
```
After launching the simulator wait for a certain time for the simulator to be ready up and running like 2 minutes depending on the specifications of your machine.

```
~path/PythonAPI/examples/python spawn_npc.py -n 100
```
This adds 100 npcs to the simulator and they move randomly within the simulator.
After the Client is able to connect to the Server and the npcs can be destroyed and the simulator launched again.
The python code RL_Adonia.py is run
```
~path/PythonAPI/examples/python RL_Adonia.py
```
This pops up a window showing the training process of the agent within the Carla environment for the a certain number of episodes. It drives within the simulator when it collides the episode is terminated and gets back on track.
After training episodes say 100 or 1000 the log events are recorded in the folder and the scalars can be visualized using a tensorboard.
These include the rewards of the agent as it explores the environment.
For Tensorboard tutorial go to https://github.com/tensorflow/tensorboard

```
~anacondapath/tensorboard --logdir = ~path/logs/tf.events
```
The graphical results are shown in the files above i.e average rewards, maximum and minimum reward for the first training of 100 episodes and also for the second training of 1000 episodes for Xception model pretrained on ImageNet dataset.

The graphical results are shown in the folders of results for both 100 and 1000 episodes, it was shown that Sequential model outperformed Xception model for during the training process as shown in the graphs. Sequential model is a 64x3 model
The graphs can be visualized at port 6006 in any browser preferrably Google chrome

The demonstration of the training using sequential model is at the following link to google drive https://drive.google.com/drive/u/1/folders/1fc8kHq-mNITIew0v-6sTC9dhsqG5KUbC

## Running the tests

run RL_Adonia.py for training and the models folder is formed under the examples folder showing how the model is improving or not
Then run RL_Agent.py and see how the agent is running generating the q-values which it uses to give a reward or penality incase of a collision.
For any errors that you may encouter visit stackoverflow at https://stackoverflow.com/

### And coding style

Python langauge due to its robustness with Machine learning algorithms

## Deployment

For deployment, a raspberry pi and pi camera with collision sensors(like Ultrasonic sensorss) will be used to deploy the model and see how it performs in an actual environment

## Built With

* [CARLA](http://carla.org/) - The simulator used
* [Anaconda](https://www.anaconda.com/distribution/) - IDE used for this particular project
* [Python](https://www.python.org/) - The programming langauage used

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [CARLA_0.9.5](http://carla.org/2019/04/03/release-0.9.5/) for versioning.

## Authors

* **Adonia Mbarebaki** - *Initial work* - https://github.com/AdoniaMbarebaki

See also the list of [contributors](https://github.com/simonry14/) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Harrison Sentdex
* 
* etc


