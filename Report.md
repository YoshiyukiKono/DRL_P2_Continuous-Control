# Project Report

## Learning Algorithm

- Deep Deterministic Policy Gradients (DDPG)


#### hyperparameters

|  Name  |  Value  |　|
| ---- | ---- | ---- |
|BUFFER_SIZE |  | replay buffer size|
|BATCH_SIZE |         | minibatch size|
|GAMMA |             | discount factor|
|TAU |               | for soft update of target parameters|
|LR |                | learning rate |
|UPDATE_EVERY |         | how often to update the network|


### The model architectures for neural networks

#### Base
- Linear(state_size, fc1_units)
- Linear(fc1_units, fc2_units)
- Linear(fc2_units, action_size)

#### Dueling Q network

- Linear(in:state size, out:64)
- Linear(in:64, out:64)
  - Value Function: Linear(64, action size)
  - Advantage Function: Linear(64, 1)
- Output = (value) + (advantage) - (the mean of advantage)

## Plot of Rewards



### The number of episodes needed to solve the environment.

|  Model  |  The number of episode  |
| ---- | ---- |
|  Base  |  |


## Ideas for Future Work


