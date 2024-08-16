# Lunar Lander with Reinforcement Learning

## Soft-Actor Critic (SAC)

![](/Images/sac_lunar_lander.gif)

## Deep Q Learning (DQN)

![](/Images/dqn_lunar_lander.gif)

## Proximal Policy Optimization (PPO)

![](/Images/ppo_lunar_lander.gif)

## Results
Hardware: Google Colab T4

| Model Type | Discrete | Average Reward| Training Time | Total Training Steps |
|------------|----------|---------------|---------------|----------------------|
| PPO        | No       | 266.01        | 1:35:29       | 501,747              |
| PPO        | Yes      | 223.38        | 2:07:30       | 501,721              |
| SAC        | No       | 257.90        | 1:36:07       | 179,285              |
| DQN        | Yes      | -61.66        | 0:41:00       | 100,000              |

## Training Notes
- Set ent_coef for PPO as it encourages exploration of other actions. Stable Baseline3 defaults the value to 0.0.
- Do not set your eval_freq too low, as it can sometimes cause instability, as the evaluation might interrupt the learning process. Try increasing the eval_freq to a higher value (e.g., 10,000) to reduce the potential disturbance to learning.


## Finding Theta Blog Posts: 
- [Solving Gymnasium's Lunar Lander with Deep Q Learning (DQN)](https://www.findingtheta.com/blog/solving-gymnasiums-lunar-lander-with-deep-q-learning-dqn)
- [Comparing how PPO, SAC, and DQN Perform on Gymnasium's Lunar Lander](https://www.findingtheta.com/blog/comparing-how-ppo-sac-and-dqn-perform-on-gymnasiums-lunar-lander)
