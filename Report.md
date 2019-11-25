# Project Report

## Learning Algorithm

- Multi Agent Deep Deterministic Policy Gradients (DDPG)

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
- Linear(in:256, out:256)
- Linear(in:256, out:256)
- Linear(in:256, out:action size)

#### Critic

- Linear(in:state size, out:256)
- Linear(in:256 + action size, out:256)
- Linear(in:256, out:256)
- Linear(in:256, out:1)


## Plot of Rewards

Refer to [Tennis.ipynb](./Tennis.ipynb)

## The number of episodes needed to solve the environment.



## Ideas for Future Work

