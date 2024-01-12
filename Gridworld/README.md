# GridWorld Reinforcement Learning Project

## Overview

This project involves the implementation and analysis of various reinforcement learning algorithms in a grid-world environment. The project contains Python scripts for running the algorithms, hyperparameter tuning, and generating results and visualizations.

## Structure

- **Gridworld/**: Contains `.py` files for the algorithms.
- **Gridworld/Data/**: Data required for running the `.py` files.
- **Results_10K_Iterations/**: Results after 10,000 iterations.
- **Results_50K_Iterations/**: Results after 50,000 iterations.
- **Hyper_Parameters/**: CSV files with different hyperparameters.
- **Final_Animation_Images/**: Final animations and plots.

## Instructions

- Run `Test-....py` files to obtain results for specific algorithms on the grid-world.
- Execute `HyperParameters.py` to check hyperparameters for each algorithm.
- Use `GenerateFinalPlots.py` to generate bar and convergence plots for algorithm comparison.

## Python File Descriptions

- **GridWorld.py**: Defines the `GridWorld` class for simulating grid-world environments.
- **GridWorldVisualizer.py**: For creating animated visualizations of algorithm training.
- **PolicyIteration.py**: Implements Policy Iteration algorithm.
- **Test-PolicyIteration.py**: Applies Policy Iteration and saves performance metrics.
- **ValueIteration.py**: Implements Value Iteration algorithm.
- **Test-ValueIteration.py**: Applies Value Iteration and saves performance metrics.
- **MCLearningES.py**: Implements Monte Carlo Learning with Exploring Starts.
- **Test-MCLearningES.py**: Applies Monte Carlo Learning and evaluates performance.
- **QLearning.py**: Implements Q-Learning algorithm.
- **Test-QLearning.py**: Applies Q-Learning and saves performance metrics.
- **DoubleQLearning.py**: Implements Double Q-Learning algorithm.
- **Test-DoubleQLearning.py**: Applies Double Q-Learning and evaluates performance.
- **TripleQLearning.py**: Implements Triple Q-Learning algorithm.
- **Test-TripleQLearning.py**: Applies Triple Q-Learning and saves performance metrics.
- **HyperParameters.py**: Explores hyperparameters for different algorithms.
- **HyperParametersCompare.py**: Compares and summarizes optimal hyperparameters.

## Hyperparameter Tuning

- Systematically explore and analyze hyperparameters for each algorithm.
- Summarize optimal hyperparameters in CSV files for reference.

## Results and Analysis

- Results are stored in the respective iteration folders (`Results_10K_Iterations`, `Results_50K_Iterations`).
- Analyze the performance of different algorithms and their variations under various conditions.

## Visualization

- Generate and view animations and plots in the `Final_Animation_Images` folder to visually understand the algorithms' behavior.

