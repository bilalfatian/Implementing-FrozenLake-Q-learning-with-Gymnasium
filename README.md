# Implementing-FrozenLake-Q-learning-with-Gymnasium


## Introduction:

Welcome to the FrozenLake Q-learning project! This repository explores the fascinating realm of reinforcement learning (RL) through the implementation of Q-learning on the FrozenLake environment. Below, you'll find an overview of Gymnasium, FrozenLake Q-learning, and the objectives of this project.

- Gymnasium:

Gymnasium serves as the foundation of this project, providing a flexible and comprehensive toolkit for RL experimentation. Developed by OpenAI, Gymnasium offers a diverse set of environments ranging from simple grid worlds to complex simulations, making it an ideal platform for RL research and development. With Gymnasium, users can easily prototype algorithms, evaluate performance, and benchmark against state-of-the-art methods.

- FrozenLake Q-learning:

FrozenLake is a classic RL environment included in Gymnasium, where an agent must navigate across a frozen lake to reach a goal tile while avoiding holes. Q-learning, a fundamental RL algorithm, is employed to learn an optimal policy for traversing the FrozenLake environment. Through trial and error, the agent updates its Q-values to make informed decisions, ultimately mastering the optimal path to the goal.

- Project Overview:

In this project, we delve into the intricacies of RL by implementing Q-learning on the FrozenLake environment using Python. We aim to explore how the agent learns to navigate the environment, analyze its performance metrics, and visualize its decision-making process. Through this journey, we gain insights into the principles of RL, the challenges of environment exploration, and the efficacy of Q-learning in solving complex tasks.

## Simulation and Visualization:

- State Distribution:

![States](https://github.com/bilalfatian/Implementing-FrozenLake-Q-learning-with-Gymnasium/assets/92918987/9e8dc71d-f170-4122-9ae3-c31c29b8c4a1)

This graph illustrates the distribution of states visited by the agent across multiple episodes in the FrozenLake environment. Each bar represents the frequency of occurrence for different states during the agent's navigation. Analyzing this distribution provides insights into the exploration pattern of the agent and the diversity of states encountered during the learning process.


- Distribution of Actions Taken by the Agent:

![Actions](https://github.com/bilalfatian/Implementing-FrozenLake-Q-learning-with-Gymnasium/assets/92918987/4bf33c1a-fd9c-426b-a284-d233fa220e54)

This graph displays the distribution of actions chosen by the agent across episodes during its exploration of the FrozenLake environment. Each bar represents the frequency of selecting a specific action (left, down, right, or up) in different states. Examining this distribution sheds light on the agent's decision-making process and the strategies it employs to navigate the environment.


- Final Frame Snapshot:

![Last-Frame](https://github.com/bilalfatian/Implementing-FrozenLake-Q-learning-with-Gymnasium/assets/92918987/a1e937ce-3dff-457e-adeb-a84d13e0319d)

This visualization presents the final frame of the FrozenLake environment after the agent has completed its navigation. The left panel shows the rendered image of the environment's state, providing a snapshot of the agent's position and surroundings at the end of the episode. The right panel depicts the learned Q-values mapped onto the grid, with arrows indicating the best action to take in each state. This snapshot offers a comprehensive view of the agent's learned policy and its understanding of the environment's dynamics.

-  Q-values and Optimal Actions:
  
![learned-Q-values](https://github.com/bilalfatian/Implementing-FrozenLake-Q-learning-with-Gymnasium/assets/92918987/f0e3ca21-e619-4864-99aa-647598e67cde)

This visualization illustrates the learned Q-values mapped onto the FrozenLake environment grid. Each cell represents a state, and the color intensity indicates the magnitude of the Q-value for that state-action pair. Additionally, arrows are overlaid to represent the best action to take in each state, based on the highest Q-value. This depiction provides insights into the agent's learned policy, highlighting the optimal actions to navigate the environment effectively.



- Steps and Rewards Evolution:

![Steps and Rewards Evolution](https://github.com/bilalfatian/Implementing-FrozenLake-Q-learning-with-Gymnasium/assets/92918987/49adb71b-a9a5-4acb-8bec-7235bd3abc8d)

This visualization presents the evolution of the agent's performance over episodes in terms of cumulative rewards and averaged steps taken. The left plot displays the cumulative rewards accumulated by the agent over time, indicating its progress in achieving positive outcomes. The right plot illustrates the average number of steps taken per episode, providing insights into the agent's efficiency in navigating the environment. Each line represents a different map size, allowing for comparisons across different scenarios. This analysis offers a comprehensive view of the agent's learning progress and performance across various environments.






- Animated GIF of Agent's Journey in the FrozenLake Environment:

![simulation](https://github.com/bilalfatian/Implementing-FrozenLake-Q-learning-with-Gymnasium/assets/92918987/7ddde81e-4715-4e9a-8f06-8498720aa7f2)

This animated GIF showcases the agent's navigation through the FrozenLake environment across multiple episodes. Each frame of the GIF captures a moment in the agent's journey, displaying its movement and interactions with the environment as it learns to navigate towards the goal. The animation provides a dynamic visual representation of the agent's exploration and learning process, offering insights into its decision-making and adaptation over time.












