# Implementing-FrozenLake-Q-learning-with-Gymnasium


## Introduction 📝

Welcome to the FrozenLake Q-learning project! This repository explores the fascinating realm of reinforcement learning (RL) through the implementation of Q-learning on the FrozenLake environment. Below, you'll find an overview of Gymnasium, FrozenLake Q-learning, and the objectives of this project.

- Gymnasium:

Gymnasium serves as the foundation of this project, providing a flexible and comprehensive toolkit for RL experimentation. Developed by OpenAI, Gymnasium offers a diverse set of environments ranging from simple grid worlds to complex simulations, making it an ideal platform for RL research and development. With Gymnasium, users can easily prototype algorithms, evaluate performance, and benchmark against state-of-the-art methods.

- FrozenLake Q-learning:

FrozenLake is a classic RL environment included in Gymnasium, where an agent must navigate across a frozen lake to reach a goal tile while avoiding holes. Q-learning, a fundamental RL algorithm, is employed to learn an optimal policy for traversing the FrozenLake environment. Through trial and error, the agent updates its Q-values to make informed decisions, ultimately mastering the optimal path to the goal.

Here's a brief overview of how Q-learning works:

1. **Initialization**: Initialize the Q-table, which is a table where each row represents a state and each column represents an action. Initially, all Q-values are set to zero.
    
2. **Exploration vs. Exploitation**: At each time step, the agent selects an action based on an exploration-exploitation trade-off. It either explores by taking a random action with probability epsilon (exploration), or it exploits by selecting the action with the highest Q-value for the current state (exploitation).
    
3. **Action Selection**: After selecting an action, the agent performs the action in the environment and observes the reward and the new state.
    
4. **Updating Q-values**: The agent updates the Q-value of the previous state-action pair using the observed reward and the maximum Q-value of the new state. The Q-value update follows the equation:

    $$Q(s,a) \leftarrow Q(s,a) + \alpha [ r + \gamma \max_a Q(s',a) - Q(s,a) ]$$

    where:
    
    *   $Q(s,a)$ is the Q-value of state-action pair $(s,a)$.
    *   $\alpha$ is the learning rate.
    *   $r$ is the reward obtained after taking action $a$ in state $s$.
    *   $\gamma$ is the discount factor, representing the importance of future rewards.
    *   $s'$ is the new state after taking action $a$.
    
5. **Repeat**: Repeat steps 2-4 for multiple episodes until convergence or a predetermined number of iterations.

By updating Q-values iteratively based on observed rewards and future Q-values, Q-learning gradually learns the optimal policy for the given environment. Over time, the agent learns to take actions that maximize long-term rewards, leading to improved performance in the task.

- Project Overview:

In this project, we delve into the intricacies of RL by implementing Q-learning on the FrozenLake environment using Python. We aim to explore how the agent learns to navigate the environment, analyze its performance metrics, and visualize its decision-making process. Through this journey, we gain insights into the principles of RL, the challenges of environment exploration, and the efficacy of Q-learning in solving complex tasks.

## Simulation and Visualization 🔮

- **State Distribution:**

![States](https://github.com/bilalfatian/Implementing-FrozenLake-Q-learning-with-Gymnasium/assets/92918987/9e8dc71d-f170-4122-9ae3-c31c29b8c4a1)

The distribution of states visited by the agent across multiple episodes in the FrozenLake environment. Each bar represents the frequency of occurrence for different states during the agent's navigation. 

In the beginning, when the agent starts exploring the environment, it tends to visit a wide range of states as it tries different actions and learns about the consequences. As a result, the distribution of visited states is relatively spread out across the state space.

However, as the agent learns and becomes more proficient in navigating the environment, it starts to converge towards a more optimal policy. This means that the agent tends to focus its exploration on states that are more likely to lead to positive outcomes, such as reaching the goal tile or avoiding holes.

States located near the edges of the environment or far from the goal may be less frequently visited because they are associated with lower rewards or higher risks. As the agent refines its policy, it prioritizes exploring states that are more promising in terms of potential rewards, leading to a decrease in the frequency of visits to states with lower utility.

- **Distribution of Actions Taken by the Agent:**

![Actions](https://github.com/bilalfatian/Implementing-FrozenLake-Q-learning-with-Gymnasium/assets/92918987/4bf33c1a-fd9c-426b-a284-d233fa220e54)

The distribution of actions chosen by the agent across episodes during its exploration of the FrozenLake environment. Each bar represents the frequency of selecting a specific action (left, down, right, or up) in different states. 

Given that the agent starts in the top-left corner of the FrozenLake environment and the goal is typically positioned towards the bottom-right corner, the shortest path to reach the goal involves moving predominantly to the right and downward.

As a result, the agent's exploration strategy tends to prioritize actions that lead it closer to the goal. Since "down" and "right" movements are more likely to advance the agent towards the target location, they are chosen more frequently during exploration. 

- **Final Frame Snapshot:**

![Last-Frame](https://github.com/bilalfatian/Implementing-FrozenLake-Q-learning-with-Gymnasium/assets/92918987/a1e937ce-3dff-457e-adeb-a84d13e0319d)

This visualization presents the final frame of the FrozenLake environment after the agent has completed its navigation. 

-  **Q-values and Optimal Actions:**
  
![learned-Q-values](https://github.com/bilalfatian/Implementing-FrozenLake-Q-learning-with-Gymnasium/assets/92918987/f0e3ca21-e619-4864-99aa-647598e67cde)

The learned Q-values mapped onto the FrozenLake environment grid. Each cell represents a state, and the color intensity indicates the magnitude of the Q-value for that state-action pair. Additionally, arrows are overlaid to represent the best action to take in each state, based on the highest Q-value. This depiction provides insights into the agent's learned policy, highlighting the optimal actions to navigate the environment effectively.



- **Steps and Rewards Evolution:**

![Steps and Rewards Evolution](https://github.com/bilalfatian/Implementing-FrozenLake-Q-learning-with-Gymnasium/assets/92918987/49adb71b-a9a5-4acb-8bec-7235bd3abc8d)

The evolution of the agent's performance over episodes in terms of cumulative rewards and averaged steps taken. 

-- The left plot displays the cumulative rewards accumulated by the agent over time, indicating its progress in achieving positive outcomes.

-- The right plot illustrates the average number of steps taken per episode, providing insights into the agent's efficiency in navigating the environment.

Each line represents a different map size, allowing for comparisons across different scenarios.


- **Animated GIF of Agent's Journey in the FrozenLake Environment:**

![simulation](https://github.com/bilalfatian/Implementing-FrozenLake-Q-learning-with-Gymnasium/assets/92918987/7ddde81e-4715-4e9a-8f06-8498720aa7f2)




## Compatibility Note for Windows Users 🖥️

If you encounter compatibility issues running the provided code in your Anaconda environment on Windows, you're not alone. Python package management and environment setup can sometimes be challenging on Windows systems due to differences in library dependencies and system configurations.

For seamless execution and hassle-free setup, I recommend using Google Colab, a cloud-based Jupyter notebook environment. Colab provides a ready-to-use Python environment with pre-installed libraries, ensuring smooth execution of the code without the need for manual installation or configuration.

To access this project in Colab, simply click [here](https://colab.research.google.com/drive/1qNuQe5AutxZTiKtpX7vvQlfKgxMNpXeT?usp=sharing) and create a copy for you, allowing you to run the code interactively in the cloud, regardless of your operating system.

You may not be able to see the GIF simulation if you open the notebook in GitHub, so I advise you to download it or to open it from this [link](https://colab.research.google.com/drive/1qNuQe5AutxZTiKtpX7vvQlfKgxMNpXeT?usp=sharing) in Colab.

## Contact me 📨

- **LinkedIn:** [Bilal Fatian](https://www.linkedin.com/in/bilal-fatian-806813254/)
- **Gmail:** [fatian.bilal@gmail.com](mailto:fatian.bilal@gmail.com)




