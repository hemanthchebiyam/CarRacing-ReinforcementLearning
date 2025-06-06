# 🚗 OpenAI Gym Car Racing Environment

## Code written by: Hemanth Chebiyam, Sanjeev Vijayakumar

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)
[![Stable Baselines3](https://img.shields.io/badge/Stable%20Baselines3-v1.0-orange)](https://stable-baselines3.readthedocs.io/en/master/)
[![OpenAI Gym](https://img.shields.io/badge/OpenAI%20Gym-v0.26-brightgreen)](https://gymnasium.farama.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-v2.0-yellow?logo=tensorflow)](https://www.tensorflow.org/)

## Certificate: Agentic AI Innovation Challenge - Ready Tensor
![](https://github.com/hemanthchebiyam/CarRacing-ReinforcementLearning/blob/main/Resources/Certificate.png)

## Introduction to Reinforcement Learning

Reinforcement Learning (RL) is a type of machine learning where an agent learns to make decisions by performing actions in an environment to maximize some notion of cumulative reward. Unlike supervised learning, where the model is trained on a fixed dataset, RL involves learning through trial and error, where the agent interacts with the environment, receives feedback, and adjusts its policy accordingly.

## Relevance of OpenAI Gym

OpenAI Gym is a toolkit for developing and comparing reinforcement learning algorithms. It provides a variety of environments ranging from classic control tasks to complex simulations, which serve as benchmarks for evaluating RL algorithms. For our use case of autonomous driving and car racing, OpenAI Gym offers the "CarRacing-v2" environment, a challenging task where an agent must learn to drive a car around a track efficiently.

## Why Use OpenAI Gym for Autonomous Driving and Car Racing?

1. **Benchmarking:** OpenAI Gym provides standardized environments, allowing us to benchmark our RL algorithms against established baselines.
2. **Complexity:** The "CarRacing-v2" environment offers a complex and dynamic scenario that simulates real-world driving challenges, making it an ideal testbed for developing robust autonomous driving agents.
3. **Flexibility:** OpenAI Gym's flexible interface allows us to experiment with different RL algorithms and adapt the environment's parameters to test various scenarios, enhancing the agent's learning and generalization capabilities.

## Overview

This repository contains an advanced reinforcement learning system designed to train agents using Deep Q-Network (DQN) and Proximal Policy Optimization (PPO) algorithms within the "CarRacing-v2" environment. The system harnesses several self-adaptive features to bolster the training efficacy and performance of the agents.

## Key Features

- **Self-Adaptive Training:** Utilizes dynamic learning rate adjustments based on agent performance.
- **Evaluation Callback:** Periodically evaluates and saves the best performing model.
- **Domain Randomization:** Introduces variability in environment parameters to enhance agent robustness.
- **GPU Acceleration:** Speeds up training using GPU resources.
- **Stable Baselines3 Integration:** Leverages state-of-the-art reinforcement learning algorithms.

## System Components

1. **Environment Setup:** Initialization of the "CarRacing-v2" environment with domain randomization and discrete mode.
2. **Agent Training:** Training agents using DQN and PPO algorithms to navigate the environment with CNN policies and custom learning rate schedules.
3. **Domain Randomization:** Varies environment parameters across episodes.
4. **RGB Rendering:** Environment rendered in RGB format.
5. **Evaluation Callback:** Periodic performance evaluation and model saving.
6. **Model Saving:** Stores the best model for future use.
7. **Animation Generation:** Creates animations of agents' performance for visualization.

## Big Picture
![](https://github.com/hemanthchebiyam/CarRacing-ReinforcementLearning/blob/main/Resources/System%20Design%20Flow.png)

### Components of the Diagram:

1. **Environment Setup:** Initialization with domain randomization, discrete mode, and RGB rendering.
2. **Agent Training:** Agents trained with DQN and PPO algorithms using CNN policies, GPU acceleration, and custom learning rate schedules.
3. **Domain Randomization:** Enhances agent's generalization ability.
4. **RGB Rendering:** Suitable for visual-based RL agents.
5. **GPU Acceleration:** Speeds up training.
6. **Custom Learning Rate Schedule:** Adjusts learning rate dynamically.
7. **Evaluation Callback:** Evaluates and saves the best model periodically.
8. **Model Saving:** Preserves the best model for future use.
9. **Animation Generation:** Visualizes agent's performance.

## PPO Algorithm Training Runs

We conducted extensive training using the PPO algorithm, with agents trained for over 2 million episodes. These runs allow us to observe the agent's performance under different conditions and draw meaningful conclusions.
Here are some visualizations of the agent's performance:

### No Training
![](https://github.com/hemanthchebiyam/CarRacing-ReinforcementLearning/blob/main/Resources/NoTraining.gif)

### 500k steps Training
![](https://github.com/hemanthchebiyam/CarRacing-ReinforcementLearning/blob/main/Resources/500k_Training.gif)

### 2 mil steps Training
![](https://github.com/hemanthchebiyam/CarRacing-ReinforcementLearning/blob/main/Resources/2mil_Training.gif)

## Quality Attributes

| Quality Attribute             | Refinement                                | Priority/Difficulty (H, M, L) | Scenario                                                                                   |
|-------------------------------|-------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------|
| Performance                   | Training efficiency                       | M                            | The agent should learn effectively within a reasonable number of episodes to navigate the CarRacing-v2 environment efficiently. |
| Performance                   | Model saving                              | L                            | The model should be saved quickly and efficiently after training to minimize downtime and ensure the learned knowledge is preserved. |
| Usability                     | Visualization                             | M                            | The visualization tools, including animations, should be easy to use and provide clear insights into the agent's performance and behavior. |
| Reliability                   | Robustness to domain randomization        | H                            | The agent should perform well and generalize across different scenarios introduced by domain randomization. |
| Maintainability               | Custom learning rate schedule             | M                            | The custom learning rate schedule should be easily adjustable and maintainable to allow for experimentation and optimization. |
| Efficiency                    | GPU acceleration                          | H                            | The use of GPU acceleration should significantly speed up the training process without compromising the quality of the learned policy. |

## Self-Adaptive System Design and Algorithm

This project exemplifies a self-adaptive system in reinforcement learning, focusing on feedback mechanisms, dynamic adjustments, and iterative improvements.

### Domain Randomization as Feedback Mechanism
- **Adaptation to Environmental Variability:** Challenges the agent to generalize across varied conditions.

### Custom Learning Rate Schedule
- **Dynamic Adjustment Based on Performance:** Optimizes learning efficiency by adjusting the learning rate.

### Evaluation and Model Saving
- **Feedback Loop for Improvement:** Identifies and retains the most effective policies.

### Visualization for Insight and Iterative Improvement
- **Iterative Learning and Adaptation:** Uses visualization tools for continuous improvement.

## 🔗 Reference

"Car Racing," Farama Gymnasium, https://gymnasium.farama.org/environments/box2d/car_racing/

