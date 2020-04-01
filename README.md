# Udacity DRLND Project 2: Continuous Control

### Introduction

In this project, we work with the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment. In this task, an agent learns to control a double-jointed arm in order to reach target locations. Reacher is a Unity ML Agents environment, and you can find out more about them [here](https://github.com/Unity-Technologies/ml-agents).  

<img src="https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif" width="400"/>

### Environment & Reward Structure
As the double-jointed arm is moved to try and reach target locations, a reward of +0.1 is provided for each time step that the agent's hand is in the goal location (balloon). The goal of the agent is therefore to learn how to move its hand in a coordinated fashion such that it accompanies the (moving) target location for as many time steps as possible.  

To achieve this goal, the agent has access to an observation space consisting of 33 continuous variables depicting the position, rotation, velocity, and angular velocities of the arm. The agent interacts with the environment by effecting an action which is described by a 4-dimensional vector corresponding to torque applicable to two joints. The entries in the action vector are continuous and bounded between -1 and 1.  

The task is episodic, with each episode running for 1,000 time steps. It is considered solved if the agent averages a score above +30 over 100 consecutive episodes.  

There are two options to the project: to solve the environment with a single agent or 20 paralellized agents. This repository contains a solution to the **single agent** option of the project. By following it, you should be able to go from a naive (left) to a pretty respectable (right) agent in under 500 episodes.   

<img align='left' width="300" src="https://github.com/andrefmsmith/drlnd_ContinuousCtrlSubmission/blob/master/NaiveAgent.gif" width="300"  /> <img align='right' src="https://github.com/andrefmsmith/drlnd_ContinuousCtrlSubmission/blob/master/ExpertAgent.gif" width="300"  />  
.  
.  
.  
.  
.  
.  
.  

### Getting Started
1. Reproduce my environment by following the instructions [here.](https://github.com/udacity/deep-reinforcement-learning#dependencies)
2. Clone this repository.
3. Download the environment (one-agent version) from whichever link below matches your operating system:
   - [Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
   - [Mac OSX](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
   - [Windows 32-bit](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
   - [Windows 64-bit](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)
4. Place the file in the same folder to which you cloned this repo, and decompress it. 

### Using this repo
['ContinuousCtrl_Report'](https://github.com/andrefmsmith/drlnd_ContinuousCtrlSubmission/blob/master/ContinuousCtrl_Report.ipynb) is a Jupyter Notebook providing a detailed code walkthrough and background for the strategy used to solve the task. To train an agent to solve this environment, open the Jupyter Notebook ['ContinuousCtrl_TrainCode'](https://github.com/andrefmsmith/drlnd_ContinuousCtrlSubmission/blob/master/ContinuousCtrl_TrainCode.ipynb) and run the code cells in it.  

Remember to change the variable env = UnityEnvironment(file_name=" "), found in the code block titled 'Set Up Environment and Key Variables', to the path pointing to your downloaded and unzipped copy of the 'Reacher' environment.  
