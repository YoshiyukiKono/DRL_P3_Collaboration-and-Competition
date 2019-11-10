# DRL_P3_Collaboration-and-Competition

## Project Details

This project is based on the section of the following github repository.

https://github.com/udacity/deep-reinforcement-learning

### Environment

![Tennis](https://video.udacity-data.com/topher/2018/May/5af7955a_tennis/tennis.png)

Please refer to [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) for details.


### Reward

In this environment, two agents control rackets to bounce a ball over a net. 
If an agent hits the ball over the net, it receives a reward of +0.1. 
If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. 
Thus, the goal of each agent is to keep the ball in play.

### State space

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. 
Each agent receives its own, local observation. 

### Action spaces

Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

### Training end condition - when the environment is considered solved

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
- This yields a single score for each episode.

The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.

## Getting Started

### Library Requirement

`requirements.txt` is included in the above-mentioned github repository.

### GPU

I used my laptop with GPU for training.

[PyTorch Quick Start](https://pytorch.org/?utm_source=Google&utm_medium=PaidSearch&utm_campaign=%2A%2ALP+-+TM+-+General+-+HV+-+JP&utm_adgroup=PyTorch+Version&utm_keyword=%2Bpytorch%20%2Bversion&utm_offering=AI&utm_Product=PyTorch&gclid=Cj0KCQjw84XtBRDWARIsAAU1aM2zq_aOaEVOMcbRXR5UUKbRyy6k2amUoQ7J8z88762R1Y5pxokc_RsaArgrEALw_wcB)

``
conda install pytorch torchvision cudatoolkit=10.1 -c pytorch
``

### Unity Environment

#### Version 2: Twenty (20) Agents
- Linux: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
- Mac OSX: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
- Windows (32-bit): [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
- Windows (64-bit): [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

## Instructions

Please refer to the following notebooks for the instructions.

Refer to [Tennis.ipynb](./Tennis.ipynb)



