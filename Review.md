# Review

## First Attempt

### tanh

>The first thing I noticed is in your actor NN model, I would recommend the output be just the tanh() of the final layer, not 10xnormalized tanh(). The output should be between -1.0 and +1.0 and tanh() gives exactly that range of values.

### sigma
>Next, in your OU noise definition, I would recommend reducing sigma to 0.1 or perhaps even 0.05. You can also reduce the scale value over time, multiplying the initial 1.0 value by a constant near one (say, 0.9995, each episode (or, something smaller even if you reduce it each mini-step rather than each episode)

Note: I realized that this comment did not meet my solution. Please refer to the following.

### from Knowledge

https://knowledge.udacity.com/questions/25366

> In the original OUNoise code of MADDPG from Udacity, the sigma=0.2 is too small, and there is a extra scale_factor=0.1.
> These made exploration noise too week.
> My experience is not using the extra scale_factor, and set sigma to 0.5, to get a more efficient exploration.

## Submission

Dear Udacian, the project is very well implemented and meets the specifications! Congratulations on successfully completing the project.
As a next step, please go through the resource: [human-like robot hand trained to manipulate physical objects with unprecedented dexterity](https://openai.com/blog/learning-dexterity/).

- A good read: [PyTorch vs TensorFlow — spotting the difference](https://towardsdatascience.com/pytorch-vs-tensorflow-spotting-the-difference-25c75777377b)

Great job providing the ideas to experiment more in future with the project!

You should try implementing Prioritized Experience Replay also. It helps to improve the performance and significantly reduces the training time. This should also help to stabilize the performance to some extent. A fast implementation of Prioritized Experience Replay is possible using a special data structure called Sum Tree. I found a [good implementation here](https://github.com/rlcode/per).

Also, I request you to check the following posts to get familiar with more reinforcement learning algorithms.

- [Asynchronous Actor-Critic Agents (A3C)](https://medium.com/emergent-future/simple-reinforcement-learning-with-tensorflow-part-8-asynchronous-actor-critic-agents-a3c-c88f72a5e9f2)
- [Trust Region Policy Optimization (TRPO) and Proximal Policy Optimization (PPO)](https://medium.com/@sanketgujar95/trust-region-policy-optimization-trpo-and-proximal-policy-optimization-ppo-e6e7075f39ed)

Here is an [implementation of PPO on tennis environment](https://github.com/jcrudy/drlnd_p3). The training was slow but the final average score achieved was almost 1.25 (with some fluctuation). You should surely try PPO in future.
