# ADVN_RoboticAI

## Introduction
In recent years, the realm of autonomous driving has experienced significant advancements, particularly in the domain of control algorithms. 
Among these algorithms, Reinforcement Learning (RL) and the Proportional-Integral-Derivative (PID) controller stand out due to their unique capabilities and applications. 

Reinforcement Learning, a branch of machine learning, enables agents to learn how to behave in an environment by performing certain actions and receiving rewards or penalties in return. 
On the other hand, the PID controller is a classical control strategy that has been widely used in numerous systems to regulate processes, ensuring that there is zero error between a desired set point and the system's output. 

Given the rapid evolution of autonomous driving technologies and the importance of ensuring robustness under varying conditions, it becomes imperative to compare the performances of these controllers in different scenarios. 

Thus, in this project, I'm going to use the CARLA simulator to compare the performances of RL and PID controller under several weather conditions. The primary purpose of this report is to determine which control strategy offers better stability and performance in various climatic challenges, paving the way for more resilient autonomous driving systems in the future.



## Install instruction
git clone this repository
```
cd ADVN_RoboticAI
conda create -n ARAI python=3.7
conda activate ARAI
pip3 install -r requirements.txt
```

Download and setup CARLA 0.9.10.1
```
chmod +x setup_carla.sh
./setup_carla.sh
easy_install carla/PythonAPI/carla/dist/carla-0.9.10-py3.7-linux-x86_64.egg
```
the setuptools==41 to install because this version has the feature easy_install.
please uninstall setuptools and install the recent setuptools

## Code usage instructions 
First run CARLA server 
```
cd ADVN_RoboticAI/carla
./CarlaUE4.sh
```
And you can run carla_env.py
The env will be determined by changing variables 'day_night' and 'rain'

day when day_night==1,night when day_night==0
Rain intensity values range from 0 to 100, being 0 none at all and 100 a heavy rain.
```
# the default is day and rainy
python3 carla_env.py
```

## Possible outcomes of the project

I will set 'rain' variable which metioned before, as 0 or 80. 
So, there could be four environments : rainy day, sunny day, rainy night and sunny night. 

Then, I'm going to use the SAC algorithm and PID controller as the agent. 
Altough the agents are not provided due to the lack of the time. It will be provided next. 

