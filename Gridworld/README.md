# GridWorld Reinforcement Learning Project

## Overview

This project involves the implementation and analysis of various reinforcement learning algorithms in a grid-world environment. The project contains Python scripts for running the algorithms, hyperparameter tuning, and generating results and visualizations.

## Structure

- **Gridworld/**: 
  -Contains `.py` files for the algorithms.
- **Gridworld/Data/**: 
  -Data required for running the `.py` files.
- **Results_10K_Iterations/**: 
  -Results after 10,000 iterations.
- **Results_50K_Iterations/**: 
  -Results after 50,000 iterations.
- **Hyper_Parameters/**: 
  -CSV files with different hyperparameters.
- **Final_Animation_Images/**:
  - Final animations and plots.

## Instructions

- Run `Test-....py` files to obtain results for specific algorithms on the grid-world.
- Execute `HyperParameters.py` to check hyperparameters for each algorithm.
- Use `GenerateFinalPlots.py` to generate bar and convergence plots for algorithm comparison.

## Python File Descriptions

This section provides an overview of each Python script in the project and their respective functionalities.

### Core Algorithms

- **GridWorld.py**
  - *Description*: Defines the `GridWorld` class to simulate grid-world environments.
- **PolicyIteration.py**
  - *Description*: Implements the Policy Iteration algorithm for Markov Decision Processes.
- **ValueIteration.py**
  - *Description*: Implements the Value Iteration algorithm for Markov Decision Processes.
- **MCLearningES.py**
  - *Description*: Implements Monte Carlo Learning with Exploring Starts, a reinforcement learning technique.
- **QLearning.py**
  - *Description*: Contains the implementation of Q-Learning, a model-free reinforcement learning algorithm.
- **DoubleQLearning.py**
  - *Description*: Implements Double Q-Learning for more stable and accurate reinforcement learning.
- **TripleQLearning.py**
  - *Description*: Implements Triple Q-Learning, enhancing reinforcement learning performance.

### Test Scripts

- **Test-PolicyIteration.py**
  - *Description*: Applies Policy Iteration on a grid-world problem, visualizing results and saving metrics.
- **Test-ValueIteration.py**
  - *Description*: Applies Value Iteration on a grid-world problem, visualizing results and saving metrics.
- **Test-MCLearningES.py**
  - *Description*: Applies Monte Carlo Learning with Exploring Starts, evaluating performance.
- **Test-QLearning.py**
  - *Description*: Applies Q-Learning on a grid-world problem, visualizing results and saving metrics.
- **Test-DoubleQLearning.py**
  - *Description*: Applies Double Q-Learning, evaluating performance.
- **Test-TripleQLearning.py**
  - *Description*: Applies Triple Q-Learning on a grid-world problem, visualizing results.

### Visualization and Analysis

- **GridWorldVisualizer.py**
  - *Description*: For creating animated visualizations of algorithm training on a grid-world.
- **HyperParameters.py**
  - *Description*: Explores hyperparameters for different reinforcement learning algorithms.
- **HyperParametersCompare.py**
  - *Description*: Compares and summarizes optimal hyperparameters.

### Utility Scripts

- **GenerateFinalPlots.py**
  - *Description*: Generates bar and convergence plots to compare the algorithms.


## Hyperparameter Tuning

- Systematically explore and analyze hyperparameters for each algorithm.
- Summarize optimal hyperparameters in CSV files for reference.

## Results and Analysis

- Results are stored in the respective iteration folders (`Results_10K_Iterations`, `Results_50K_Iterations`).
- Analyze the performance of different algorithms and their variations under various conditions.

## Visualization

- Generate and view animations and plots in the `Final_Animation_Images` folder to visually understand the algorithms' behavior.

