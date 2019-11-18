# Collaboration and Competition

## 1. Introduction

The goal of this project is to solve the Tennis Environment of the Unity ML-Agents framework. In fact it means you have to teach an agent to control rackets to bounce a ball over a net and to play against itself. However there are two separate agents in the game, they belong to the same class and instance.

This short animation below shows how agent plays in that environment. However the design of that scene looks a bit different nowadays, the goal is just the same.

![Tennis Environment - nowadays it looks differently](https://user-images.githubusercontent.com/10624937/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif)

[source](https://user-images.githubusercontent.com/10624937/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif)

## 2. Some details

If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores. This yields a single score for each episode. The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

## 3. My solution

I decided to solve this task with one single agent instance that plays both roles simultaneously. Since I provide the GPU time for myself I decided to run a longer training with a more slim model.

You cen find a report about my solution in details in the `Report.html` file. Some additional information is available in the file `Report.md` if the output of the jupyter-notebook aint clear enough for you.

If you want to run my solution on your machine or at any place in that cloudy world `Tennis.ipynb` is the file you're searching for.

If you want to jump right into the origins of the project `Tennis_Original.ipynb` is definitely your best friend now.

### 3.1. How to install

To use this code you need a Python environmnet, some additional Python modules and some binearies of the Unity Environment. The concrete binaries depend on your operating system or on the cloud which you're using.

#### 3.1.1. Python Environment

You can get simple **Python** with `pip` from [here](https://www.python.org/downloads/).

Or you can get **Anaconda**, which is a more complex Python environment from [here](https://www.anaconda.com/distribution/).

If you aren't afraid of paying for Python environmnet or you're familiar with JetBrains stuff **PyCharm** is your solution. You can get it from [here](https://www.jetbrains.com/pycharm/).

There are many other solutions to work with Python, run and edit Python stuff. Even clouds of **Amazon**, of **Google** and of other providers offer that kind of solutions for free or for some money as well.

If none of tham are familiar for you, I consider to visit other resource which are more convinient for your actual experience and come back later to enjoy this project too.

#### 3.1.2. Additional Python modules

You can simply install additional Python modules from `requirements.txt` with the command `pip install -r requirements.txt`.

However if you want to have a more powerful solution I recommend you to install **PyTorch** before anything else. It'll install most of the requiremnets by the way. You can select the most convinient PyTorch version from [here](https://pytorch.org/). You can select parameters in the *Quick Start Locally* section. Please take a look at the CUDA section since it can fasten your performance very well if you have a compatible GPU in your computer.

#### 3.1.3. Binaries for Unity Environmnet

Download the environment from one of the links below.  You need only select the environment that matches your operating system:

  - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
  - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
  - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
  - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
    
(_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

(_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux_NoVis.zip) to obtain the "headless" version of the environment.  You will **not** be able to watch the agent without enabling a virtual screen, but you will be able to train the agent.  (_To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the **Linux** operating system above._)

### 3.2. Try the solution - run the code

If you want to test my solution you can run anything but part `3.5.` in the file `Tennis.ipynb`.

### 3.3. Play around

If you want to see how parameters change the learning process you're welcome to play with the numbers in section `3.2.1.`.

## 4. Improvement ideas

There are several ways to imporve the performance the code in this environment. I'll plan to implement all of them. And there is another similar environment to play with. I plan to code it as well.

### 4.1. Train for the 1.0 rule

I plan to train the same network untill the average of the last 100 episodes reaches **1.0**.

### 4.2. Soccer Challenge

I plan to solve the **Crawler Environment** too, where the goal is to train a team of agents to play soccer.

![It's pretty nice. Isn't it?](https://user-images.githubusercontent.com/10624937/42135622-e55fb586-7d12-11e8-8a54-3c31da15a90a.gif)

[source](https://user-images.githubusercontent.com/10624937/42135622-e55fb586-7d12-11e8-8a54-3c31da15a90a.gif)
