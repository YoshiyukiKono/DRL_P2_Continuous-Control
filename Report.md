# Project Report

## Learning Algorithm

- Deep Deterministic Policy Gradients (DDPG)

### hyperparameters

|  Name  |  Value  |　|
| ---- | ---- | ---- |
|BUFFER_SIZE | 1e5 | replay buffer size|
|BATCH_SIZE | 1024        | minibatch size|
|GAMMA | 0.99        | discount factor|
|TAU | 1e-3              | for soft update of target parameters|
|LR_ACTOR | 1e-4               | learning rate of the actor |
|LR_CRITIC | 1e-3               | learning rate of the critic |
|WEIGHT_DECAY | 0        | L2 weight decay |


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

- the agent is able to receive an average reward (over 100 episodes, and over all 20 agents) of at least +30.

Refer to [Continuous_Control_multi.ipynb](./Continuous_Control_multi.ipynb)

## The number of episodes needed to solve the environment.

|    |  The number of episode  | Average score |
| ---- | ---- | ---- |
|  Least episode | 260 | 32.25 |
|  Highest score  | 340 | 34.20 |


## Ideas for Future Work

- Use another algorithm, e.g. PPO(Proximal Policy Optimization) 

