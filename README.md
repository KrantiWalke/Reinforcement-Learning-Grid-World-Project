# Reinforcement-Learning-Grid-World-Project

### 1. Motivation

The motivation behind this project was to delve into the intricate world of reinforcement learning by engaging with a complex grid world environment. This environment, with its unique states, obstacles, and reward structures, offered a practical and challenging platform to apply and compare various reinforcement learning strategies. Our aim was to not only understand the dynamics of different algorithms like Policy Iteration, Value Iteration, Monte Carlo Learning, and Q-Learning but also to evaluate their effectiveness in navigating through an environment filled with strategic decisions and potential pitfalls. The project served as a means to grasp the fundamental concepts of reinforcement learning and to witness firsthand how different approaches fare in a controlled yet unpredictable setting.

### 2. Problem Statement

The task involved tackling an (8x8) grid world environment characterized by distinct states: the starting state denoted by Yellow, the end state marked as Green, and the absorbing states encompassing Green and Red (Trap). The grid contained impassable areas represented by Black states, shaping the exploration. Reward structures were established, assigning +1 for achieving the goal, -1 for falling into the trap, and a consistent -0.02 for all other state transitions, defining the dynamics of movement. Actions available to navigate this environment were limited to four: Left, Right, Up, and Down, shaping the agent's permissible movements within the grid.

![image](https://github.com/KrantiWalke/Reinforcement-Learning-Grid-World-Project/assets/72568005/85ff9dee-47b3-4581-977d-5ec8582c77d5)


### 3. Background

In our foundational exploration of reinforcement learning, we focused on key pillars of understanding. We began by examining the Bellman Equations for State Values and Action Values (Q-function). These equations define the relationship between state or action values and subsequent states, fundamental in determining optimal strategies. Our journey continued with Policy Iteration, a systematic method refining policies through evaluation and enhancement, and Value Iteration, aimed at iteratively determining optimal value functions. Additionally, we explored Q-learning, a cornerstone algorithm enabling adaptive decision-making in dynamic environments. These elements are fundamental in shaping our approach to tackling intricate challenges in reinforcement learning.

### 4. Approach

TThe "GridWorld" class serves as the foundation for a Markov Decision Process (MDP) environment, featuring a grid world with diverse cell types. It initializes the grid from a CSV file, computes the reward function, and constructs a transition model considering both deterministic and random actions. The class enables simulation of transitions within the MDP framework. We applied diverse Optimal Control methods, including Policy Iteration, Value Iteration, Monte Carlo (Exploring Starts), and Temporal Difference, for Grid World problem-solving. We also explored Q-learning, Double Q-learning, and Triple Q-learning to learn optimal policies in this complex environment
The "PolicyIteration" class implements the Policy Iteration algorithm, incorporating essential components for policy evaluation and improvement. The iterative training method guarantees convergence or a specified maximum number of iterations, updating policies based on expected future rewards. 

Similarly, the "ValueIteration" class represents the Value Iteration algorithm, iteratively updating state values to determine optimal policies. Both classes utilize zeros as initial state values and visualize convergence metrics.
The Monte Carlo Learning with Exploring Starts (MCLearningES) algorithm features key components such as a Q-table, Policy table, and a count table for state-action pairs. During episodic training, it employs a backward update of Q-values, considering every visit to states. The "policy_update" method refines the policy based on Q-values, with design choices including random policy initialization and visualization of updates. The algorithm converges iteratively by refining policies, providing insights into rewards and winning percentages over training epochs.

In the Q-Learning algorithm encapsulated in the "QLearning" class, key components include a Q-table and a randomly initialized policy. The agent undergoes episodic training, updating Q-values using the temporal difference (TD) approach based on rewards and future estimates. The "e_greedy" method balances exploration and exploitation, converging iteratively by refining policies through the Q-Learning formula.

In the Double Q-Learning and Triple Q-Learning algorithms, the core components and training strategies exhibit similarities to the Q-Learning approach. Double Q-Learning introduces the concept of employing two Q-tables and corresponding policies, a design aimed at mitigating the potential overestimation bias that can occur in traditional Q-Learning. This modification enables a more balanced assessment of action values during training. Building upon this concept, Triple Q-Learning extends the paradigm to incorporate three Q-tables and policies, further enhancing the reduction of bias in value estimates. The training process for both Double Q-Learning and Triple Q-Learning remains episodic, with the agent repeatedly interacting with the environment and updating its Q-values using the temporal difference (TD) approach. Rewards received during episodes and the agent's future estimates are crucial in shaping the Q-values. To strike a balance between exploration and exploitation during training, both variants employ the "e_greedy" method, which governs the agent's actions.

### 5. Evaluation Strategy
#### 5.1 Metrics
The performance of each algorithm was assessed and compared using two key metrics: the average reward and the time taken for convergence, measured in seconds. The average reward metric evaluated the effectiveness of the resulting policy in guiding an agent to accumulate rewards during a simulated journey in the grid world. The convergence time was employed to gauge the speed at which each algorithm arrived at its final policy.

Furthermore, the variance in performance for each algorithm was considered. This involves measuring how consistent the algorithm's performance is across different runs or settings. A lower variance indicates more consistent performance, while a higher variance suggests greater fluctuation in effectiveness.

Moreover, the average time taken per iteration for each algorithm was also taken into account. This metric provides insight into how efficiently an algorithm processes each step or iteration during its policy development, offering a more granular view of its computational efficiency.


#### 5.2 Hyper-Parameter Optimization

To accurately assess and contrast the various Reinforcement Learning algorithms, it was necessary to identify the most effective learning parameters for each. To achieve this, we systematically explored the hyper-parameter combinations. The hyper-parameters we examined are detailed below:  

![image](https://github.com/KrantiWalke/Reinforcement-Learning-Grid-World-Project/assets/72568005/71c1da8f-44a3-46a1-98d3-2eb098ce4329)

For Policy Iteration (PI) and Value Iteration (VI), the chosen parameters included gamma and tolerances. In the case of Monte Carlo with Exploring Starts (MC w/ ES), the parameters were the total number of episodes and the length of each episode. The inclusion of an Episode Length parameter was particularly important to cap the maximum actions in an episode, addressing situations where agents, despite avoiding traps, would take excessively long to finish an episode due to suboptimal performance. For Temporal Difference (TD) methods, the parameters involved were gamma, alpha, epsilon, and the total count of episodes.


#### 5.3 Average Reward

We applied different reinforcement learning algorithms (Policy Iteration, Value Iteration, Monte Carlo, Q-Learning, Double Q-Learning, and Triple Q-Learning) to a Grid World scenario. For each algorithm, we:

✔ Trained the model to develop a policy.

✔ Assessed this policy over multiple episodes.

✔ Determine the average reward by averaging the rewards from multiple evaluation episodes.

✔ Repeated training and evaluation multiple times per algorithm, using different seeds or initial conditions, to ensure robustness in the calculated average rewards.

✔ Compared the performance of each algorithm based on these average reward metrics

### 6. Evaluation Results and Comparative Analysis 

#### 6.1 Optimal Hyper-Parameters

The optimal hyper-parameters were found for each algorithm:

![image](https://github.com/KrantiWalke/Reinforcement-Learning-Grid-World-Project/assets/72568005/e5330547-2364-4d91-9882-bc4407b4ca20)

#### 6.2 Average Reward

![image](https://github.com/KrantiWalke/Reinforcement-Learning-Grid-World-Project/assets/72568005/ef0bcd62-0310-4fe5-a782-56c06d9d3022)

✔ Optimal Control Methods: Significantly fastest among all tested methods.

✔ Monte Carlo (ES): Notably the slowest in comparison.

✔ Q-Learning: Demonstrates faster performance than Monte Carlo methods.

✔ Double Q-Learning: Yields nearly identical results to Q-Learning.

✔ Triple Q-Learning: Fails to outperform Double Q-Learning.

![image](https://github.com/KrantiWalke/Reinforcement-Learning-Grid-World-Project/assets/72568005/cc703482-b21e-468a-94dc-87ff78034bb9)


#### 6.3 Average Time per Iteration

![image](https://github.com/KrantiWalke/Reinforcement-Learning-Grid-World-Project/assets/72568005/b5b407fe-2b0f-472c-bb05-f9cbdd2886c5)

#### 6.4 Time Taken

The time taken for each of the algorithms to converge on a policy is provided below:

![image](https://github.com/KrantiWalke/Reinforcement-Learning-Grid-World-Project/assets/72568005/2ceeb088-b066-4992-a550-bb0dbb577ec3)


#### 6.5 Results: Post 50K Iterations

![image](https://github.com/KrantiWalke/Reinforcement-Learning-Grid-World-Project/assets/72568005/2166f1ae-c38c-4b7b-a0d8-3103e99b88de) ![image](https://github.com/KrantiWalke/Reinforcement-Learning-Grid-World-Project/assets/72568005/0847ef3c-4ee1-4e70-b428-b0b500cefb57)

### 7. Conclusion 

In our exploration of Optimal Control Methods, a standout was the significant speed exhibited by one particular approach, surpassing all tested methods in terms of efficiency. Monte Carlo (ES), on the contrary, emerged as notably the slowest among the methods compared. Q-Learning demonstrated faster performance when juxtaposed with Monte Carlo methods, showcasing its efficiency in navigating this space. Meanwhile, Double Q-Learning yielded results nearly identical to Q-Learning, indicating a parallel performance between the two methodologies. However, Triple Q-Learning fell short in outperforming Double Q-Learning, highlighting its limitations in achieving superior results within this context. In comparison to Q learning, Double Q-Learning and Triple Q-Learning performed better when we used 50,000 episodes. 

Some Insights:

✔ Value and Policy Iteration: Excel in well-known environment dynamics.

✔ Q-Learning Variants: Adapt well to complex or unknown dynamics.

✔ Hyperparameter Tuning: Critical for RL algorithm success.

✔ Exploration Strategies: Essential for effective learning.


### 8. Future Work

In future developments of this project, exploring additional algorithms could provide a more comprehensive understanding and comparison. Enhancements to existing algorithms, as well as the creation of hybrid models, could lead to improvements in both efficiency and accuracy. Increasing the complexity of grid world environments and introducing dynamic elements during training could serve to test the adaptability and robustness of various algorithms. Employing advanced hyperparameter optimization techniques, like Bayesian optimization, alongside a broader exploration of hyperparameter values, could optimize algorithm performance. Introducing sophisticated performance metrics and conducting detailed statistical analyses would offer deeper insights into the differences between algorithms. Additionally, testing the scalability of these algorithms in larger, real-world scenarios and across various domains, such as robotics or automated decision-making systems, would be valuable. Assessing the generalization capabilities of algorithms in new, unseen environments, and their robustness against environmental noise or perturbations, could also provide important insights into their practical applicability.
