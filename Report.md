# Project Report

## Learning Algorithm

- Multi Agent Deep Deterministic Policy Gradients (DDPG)
  - 2 Actors, which uses the experiences of a player
  - 1 Critic, which uses the experiences of both players

### hyperparameters

#### Values after the change
|  Name  |  Value  |　|
| ---- | ---- | ---- |
|BUFFER_SIZE | 1e6 | replay buffer size|
|BATCH_SIZE | 1024        | minibatch size|
|GAMMA | 0.99        | discount factor|
|TAU | 1e-3              | for soft update of target parameters|
|LR_ACTOR | 1e-4               | learning rate of the actor |
|LR_CRITIC | 1e-3               | learning rate of the critic |
|WEIGHT_DECAY | 0        | L2 weight decay |

#### Values before the change
|  Name  |  Value  |　|
| ---- | ---- | ---- |
|LR_CRITIC | 31e-4               | learning rate of the critic |
|WEIGHT_DECAY | 0.0001        | L2 weight decay |

### OU Noise

Ornstein-Uhlenbeck process.

#### Values after the change
|  Name  |  Value  |　|
| ---- | ---- | ---- |
| mu | 0               |  |
| theta | 0.15        |  |
| sigma | 0.5        |  |
| noise (used with sigma) |  (np.random.standard_normal)        |  |

#### Values before the change
|  Name  |  Value  |　|
| ---- | ---- | ---- |
| sigma | 0.2, 0.05        |  |
| noise (used with sigma) |  (random.random)        |  |

### The model architectures for neural networks

#### Actor

- Linear(in:state size, out:256)
- Linear(in:256, out:action size)

#### Critic

- Linear(in:state size x 2, out:256)
- Linear(in:256 + action size x 2, out:256)
- Linear(in:256, out:256)
- Linear(in:256, out:1)


## Plot of Rewards

Refer to [Tennis.ipynb](./Tennis.ipynb)

## The number of episodes needed to solve the environment.

The agents got an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents) with around 2300 episodes.

## Project History

### First Attempt: 
First, I tried to utilize the implementation from 15. MADDPGLab of Lesson 2 Introduction to Multi-Agent RL.

[Tennis_first_attempt.ipynb](./Tennis_first_attempt.ipynb)
Although I managed to run it after I modified, the multi agent DDPG never learn at all.

### Second Attempt: Original Implementation of multi agent DDPG
Then, I implemented my version of multi agent DDPG based on DDPG for Project 2.
It did not seem to work as expected.

### Third Attempt: "simple" DDPG
With the , I checked some Knowledge articles and got an idea from my mentor, I saw that multi agent DDPG was not necessarily needed for this project.
I managed to realize a meaningful result with using two agents, which are ported from Project 2.

[Tennis_simple.ipynb](./Tennis_simple.ipynb)

### Last Attempt:

After the third attempt, I realized that the values of some parameters were different between the second (and first) attempt and the successful third attempt. So I used the values of the DDPG versiont for the multi-agent DDPG.
Finally, I faced a successfull result, which is far better than the simple version.

## Remarks

In the third attempt, I used two completely separate DDPG agents which do not share experiences. 
The DDPG agents worked well. But I'm aware of the following sentences from  "Some Hints" in "5. Benchmark Implements" of the "Collaboration and Competition" project.

>each agent receives its own, local observation. each agent used the same actor network to select actions, and the experience was added to a shared replay buffer.

Even though a shared experience for a shared network should be effective, it is just a matter of learning time.

## Ideas for Future Work

- More performance tuning for improving the agent's performance.
- Try miner changes and compare the results for the two types of implementation, DDPG and multi-agent DDPG
- Try to find and implement other algorithmes for cooperative/hostile situation.

