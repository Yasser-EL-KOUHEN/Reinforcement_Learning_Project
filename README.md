# Reinforcement_Learning_Project

## Notebook 1: Reinforcement Learning Basics and Reservoir Water Level Control

### Overview
This notebook introduces the fundamental concepts of Reinforcement Learning (RL), including theoretical comprehension, a multiple-choice questionnaire, and a practical example involving water level management in a cooling reservoir.

### Content
- **Theoretical Questions**: 
  - Differences between reinforcement, supervised, and unsupervised learning.
  - Essential components of reinforcement learning.
  - Types of policies (deterministic vs. stochastic).
  - Role of the discount factor (gamma).
  - Explanation and steps of policy gradient methods (REINFORCE algorithm).

- **Multiple-choice Questionnaire (MCQ)**: Testing knowledge about:
  - State representation
  - Policies
  - Value and Q-functions

- **Practical Application: Cooling Reservoir Water Level**
  - **Problem Description**: Maintaining optimal water levels between 4 and 8 liters, with strict limits from 0 to 12 liters.
  - **Actions**: Add or remove water, with random quantities between 0 and 0.5 liters.
  - **Reward Function**:
    - Optimal range (4–8 liters): +1
    - Acceptable range (0–4 or 8–12 liters): -0.5
    - Out-of-bound levels: -10

- **Implementation**:
  - Environment modeling
  - Policy network using PyTorch
  - Training the agent with the REINFORCE algorithm
  - Visualization and evaluation of results

---

## Notebook 2: Reinforcement Learning on a 5×5 Grid

### Overview
In this notebook, an RL agent learns to navigate a 5×5 grid, starting from (0,0) and aiming to reach the target at (4,4) using the REINFORCE algorithm.

### Content
- **Environment Description**:
  - Grid size: 5×5
  - Starting position: (0,0)
  - Target position: (4,4)

- **Possible States**:
  - All grid positions from (0,0) to (4,4), total 25 states.

- **Actions**:
  - Move Up, Down, Left, or Right. Attempting to move outside the grid leaves the agent stationary.

- **Reward Function**:
  - Reaching the target: +1
  - Any other step: -1

- **REINFORCE Algorithm Implementation**:
  - **Neural Network Representation**:
    - Input: agent's coordinates (x, y)
    - Hidden Layer: 128 neurons, ReLU activation
    - Output Layer: 4 neurons (action probabilities), softmax activation

  - **Stochastic Policy**:
    - Encourages exploration by selecting actions based on probabilities.
    - Gradients estimated via sampled trajectories.

  - **Policy Updates**:
    - Episodes generated to calculate cumulative returns.
    - Weight updates through gradient ascent based on returns.

- **Experimentation and Analysis**:
  - Metrics used: success rate, average steps to target, cumulative reward.
  - Visualization of learned policies using action symbols.

- **Adaptations for Larger Grid (10×10)**:
  - Suggested changes include increasing neural network complexity, adjusting learning rates, enhancing exploration strategies, and using variance reduction techniques.

---

### Usage
Each notebook can be executed independently. Ensure all dependencies (PyTorch, Gymnasium, NumPy, Matplotlib) are installed prior to running.

---

### Dependencies
- Python
- PyTorch
- Gymnasium
- NumPy
- Matplotlib
