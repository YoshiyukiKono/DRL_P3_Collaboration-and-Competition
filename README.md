# DRL_P3_Collaboration-and-Competition

## Project Details

This project is based on the section of the following github repository.

https://github.com/udacity/deep-reinforcement-learning

### Environment

![Reacher](https://video.udacity-data.com/topher/2018/June/5b1ea778_reacher/reacher.gif)

Please refer to [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) for details.

### Reward

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

### State space

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. 

### Action spaces

Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

### Training end condition - when the environment is considered solved

#### Option 1
The task is episodic, and in order to solve the environment, your agent must get an average score of +30 over 100 consecutive episodes.

#### Option 2
The barrier for solving the second version of the environment is slightly different, to take into account the presence of many agents. In particular, your agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). Specifically,

- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 20 (potentially different) scores. We then take the average of these 20 scores.
- This yields an average score for each episode (where the average is over all 20 agents).

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

#### Version 1: One (1) Agent
- Linux: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
- Mac OSX: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
- Windows (32-bit): [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
- Windows (64-bit): [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)
#### Version 2: Twenty (20) Agents
- Linux: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
- Mac OSX: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
- Windows (32-bit): [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
- Windows (64-bit): [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

## Instructions

Please refer to the following notebooks for the instructions. Option 2 has the final result.

### Option 1

Refer to [Continuous_Control_single.ipynb](./Continuous_Control_single.ipynb)

### Option 2

Refer to [Continuous_Control_multi.ipynb](./Continuous_Control_multi.ipynb)

## (Optional) Build your Own Environment
If you are interested in learning to build your own Unity environments, you are encouraged to follow the instructions [here](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Getting-Started-with-Balance-Ball.md), which walk you through all of the details of building an environment from a Unity scene.

