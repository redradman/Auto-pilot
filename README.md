# Auto-Pilot / LunarLander-v3
Auto-Pilot / LunarLander-v3** is a reinforcement learning project that leverages [[Deep Q-Network (DQN) algorithm](https://arxiv.org/abs/1312.5602)](https://arxiv.org/abs/1312.5602) to **train an autonomous agent to land a ship safely without collision**. 

Utilizing the [LunarLander-v3](https://gymnasium.farama.org/environments/box2d/lunar_lander/) environment from Gymnasium, the agent must learn to land the ship in the designated spot without crashing into the two yellow flags. **The agent learns how to do this using the rewards (numeric feedback) it receives for its actions.**

## Table of Contents
- [Auto-Pilot / LunarLander-v3](#auto-pilot--lunarlander-v3)
  - [Table of Contents](#table-of-contents)
  - [Results](#results)
  - [Features](#features)
  - [Environment](#environment)
    - [What the learning agent can see](#what-the-learning-agent-can-see)
    - [What the agent can do](#what-the-agent-can-do)
  - [Installation](#installation)

## Results
Let's skip to results: 
| Before Training | After Training |
|:--------------:|:-------------:|
| | |
| Episode 0: The ship simply collapses since the agent has not interacted with the environment and not learned anything yet | **After 500 epsiodes** (iteration of training), the agent has learned to slowly land the ship between the yellow flags|

## Features
- **Deep Q-Network (DQN) Implementation**: Customizable DQN target network for stable learning. **In this project,DQN algorithm has been implemented from scratch without any dependencies** from the [original paper](https://arxiv.org/abs/1312.5602) (look at algorithm 1 in the paper for the pseudocode).
- **Advanced Replay Buffer Management**: Enhanced buffer training frequency to optimize learning rates. Replay buffer is used to store the experiences of the agent during training.
- **Comprehensive Documentation**: Detailed README with environment setup, feature descriptions, and usage guidelines.
- **Performance Logging and Visualization**: Track training progress and visualize results for better insights.

## Environment
The environment is a [LunarLander-v3](https://gymnasium.farama.org/environments/box2d/lunar_lander/) from Gymnasium.

### What the learning agent can see
This table provides a detailed description of the key features used in the lander environment, which are critical for controlling and observing the state of the lander during its descent and landing. 

| Index | Feature                                                           | Description                                         |
| ----- | ----------------------------------------------------------------- | --------------------------------------------------- |
| 0     | **Horizontal pad coordinate (x)**                                 | Horizontal position of the lander (x-axis)          |
| 1     | **Vertical pad coordinate (y)**                                   | Vertical position of the lander (y-axis)            |
| 2     | **Horizontal speed (x)**                                          | Speed of the lander along the x-axis                |
| 3     | **Vertical speed (y)**                                            | Speed of the lander along the y-axis                |
| 4     | **Angle**                                                         | Rotation angle of the lander                        |
| 5     | **Angular speed**                                                 | Rotational speed of the lander                      |
| 6     | **If the left leg contact point has touched the land (boolean)**  | Whether the left leg has made contact (True/False)  |
| 7     | **If the right leg contact point has touched the land (boolean)** | Whether the right leg has made contact (True/False) |

### What the agent can do
This table outlines the possible actions the agent (who is learning) can take during the descent and landing of the ship. 

| Index | Action                            | Description                             |
| ----- | --------------------------------- | --------------------------------------- |
| 0     | **Do nothing**                    | The lander remains idle                 |
| 1     | **Fire left orientation engine**  | Rotates the lander to the right         |
| 2     | **Fire the main engine**          | Fires the main engine to propel upwards |
| 3     | **Fire right orientation engine** | Rotates the lander to the left          |



## Installation

