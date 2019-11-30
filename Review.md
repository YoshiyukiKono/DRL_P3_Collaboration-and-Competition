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
