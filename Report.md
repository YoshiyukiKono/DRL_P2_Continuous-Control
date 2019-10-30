# Project Report

## Learning Algorithm

- Deep Q-Network
  - Dueling Network
  - Double DQN
  - Prioritized Experience Replay

#### hyperparameters

|  Name  |  Value  |　|
| ---- | ---- | ---- |
|BUFFER_SIZE | int(1e5)  | replay buffer size|
|BATCH_SIZE | 64         | minibatch size|
|GAMMA | 0.99            | discount factor|
|TAU | 1e-3              | for soft update of target parameters|
|LR | 5e-4               | learning rate |
|UPDATE_EVERY | 4        | how often to update the network|


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

A plot of rewards per episode is included to illustrate that the agent is able to receive an average reward (over 100 episodes) of at least +13. 

### The number of episodes needed to solve the environment.

|  Model  |  The number of episode  |
| ---- | ---- |
|  Base  |  729|
|  Dueling Q Network  |  794  |
|  Double DQN  |  616  |
|  Prioritized Experience Replay  |  659  |

## Ideas for Future Work

- Use different network patterns
- Improve prioritized experience replay
  - Use differenct constructions, e.g. the timing to update the memory, and how to update the memory
- Try a different input to the model (output from the game), i.e. bitmap image
