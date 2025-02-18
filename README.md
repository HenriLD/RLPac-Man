# Reinforcement Learning for Pac-Mac AI

This project explores various reinforcement learning (RL) techniques by developing an agent that plays a dynamic variant of Pac-Man. The goal is to create an environment that retains classic gameplay mechanics—such as pellet consumption, power-ups, and ghost avoidance—while introducing stochastic elements and multiple RL approaches to tackle the problem.

---

## Table of Contents

- [Motivation and Problem Definition](#motivation-and-problem-definition)
- [Environment Description](#environment-description)
- [Implemented Agents and Approaches](#implemented-agents-and-approaches)
- [Implementation Details](#implementation-details)
- [Results and Analysis](#results-and-analysis)
- [References](#references)
- [Contact Information](#contact-information)

---

## Motivation and Problem Definition

The objective of this project is to develop an RL agent capable of playing a Pac-Man variant in a more dynamic environment. Rather than implementing a full-fledged Pac-Man game, the focus is on a grid-based simulation that incorporates key game mechanics along with additional challenges such as:

- Stochastic ghost movements that introduce unpredictability.
- Multiple RL approaches to compare performance and learning dynamics.

This framework enables the demonstration of core RL concepts while remaining closely aligned with established research in video game AI :contentReference[oaicite:0]{index=0}.

---

## Environment Description

### State Space

- **Grid-based Representation:** The game is represented on a grid where each cell may contain food (pellets), power-ups, or ghosts.
- **Encoded Information:** The state includes Pac-Man’s position, ghost locations, food positions, and the availability of power-ups.

### Action Space

- The agent can move in four directions:
  - Up
  - Down
  - Left
  - Right

### Rewards

- **Pellet Consumption:** +10 points
- **Fruit Consumption:** +50 points
- **Ghost Capture:** +200 points (when a power-up is active)
- **Caught by a Ghost:** -100 points
- **Level Completion:** +500 points

---

## Implemented Agents and Approaches

The project investigates multiple RL methodologies to determine the most effective approach for the game environment:

- **Q-learning:** Serves as a baseline to evaluate traditional tabular methods.
- **Deep Q-Network (DQN):** Addresses larger state spaces through deep learning.
- **Proximal Policy Optimization (PPO):** Allows a comparative analysis between value-based and policy-based learning methods.

Additional exploration may include using CNN-based state representations to determine if learning directly from visual inputs can further improve performance.

---

## Implementation Details

- **Environment Setup:** 
  - Built using [gymnasium](https://gymnasium.farama.org) (formerly OpenAI Gym) for simulation.
  - Uses [pygame](https://www.pygame.org/) to create interactive visualizations.
- **Dynamic Elements:** 
  - Introduces stochastic ghost movement for increased challenge.
- **Training Enhancements:** 
  - Incorporates reward shaping and transfer learning to improve training efficiency.
- **Evaluation:** 
  - Performance is assessed through reward curves over training episodes.
  - Visualizations help analyze agent behavior and decision-making.
  - Comparative metrics include sample efficiency, convergence speed, and final performance outcomes.
- **Ablation Study:** 
  - Investigates the impact of different state representations, the effect of randomness, and hyperparameter tuning.

---

## Results and Analysis

The project includes thorough visualization and comparative analysis:

- **Training Performance:** 
  - Reward curves plotted over episodes to monitor learning progress.
- **Agent Behavior:** 
  - Visual representations of learned policies to evaluate movement patterns.
- **Comparative Analysis:** 
  - Evaluation of Q-learning, DQN, and PPO with respect to performance metrics.
- **Ablation Studies:** 
  - Detailed analysis on the influence of various design choices on agent effectiveness.

---

## References

1. Sutton, R. S. (2018). *Reinforcement Learning: An Introduction*. A Bradford Book.
2. OpenAI Gym documentation: [https://gymnasium.farama.org](https://gymnasium.farama.org)
3. Mnih, V., et al. (2015). *Human-level Control through Deep Reinforcement Learning*. Nature, 518(7540), 529-533.
4. Schulman, J., et al. (2017). *Proximal Policy Optimization Algorithms*. arXiv preprint arXiv:1707.06347.

---

## Contact Information

- **Ludovic Nicoud**  
  CentraleSupélec  
  3 Rue Joliot Curie, 91190 Gif-sur-Yvette  
  Email: [Ludovic.Nicoud@student-cs.fr](mailto:Ludovic.Nicoud@student-cs.fr)

- **Zacharie Fredj**  
  CentraleSupélec  
  Email: [Zacharie.Fredj@student-cs.fr](mailto:Zacharie.Fredj@student-cs.fr)

- **Henri Langlois**  
  CentraleSupélec  
  Email: [Henri.Langlois@student-cs.fr](mailto:Henri.Langlois@student-cs.fr)
