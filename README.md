# Lunar Lander with Reinforcement Learning

## Soft-Actor Critic (SAC)

![](/Images/sac_lunar_lander.gif)

## Deep Q Learning (DQN)

![](/Images/dqn_lunar_lander.gif)

## Proximal Policy Optimization (PPO)

![](/Images/ppo_lunar_lander.gif)

## Results
Hardware: Google Colab T4

| Model Type | Discrete | Average Reward| Training Time | Total Training Steps | HuggingFace Repo                                                   |
|------------|----------|---------------|---------------|----------------------|--------------------------------------------------------------------|
| PPO        | No       | 266.01        | 1:35:29       | 501,747              | [Link](https://huggingface.co/kuds/rl-lunar-lander-ppo)            |
| PPO        | Yes      | 223.38        | 2:07:30       | 501,721              | [Link](https://huggingface.co/kuds/rl-lunar-lander-continuous-ppo) |
| SAC        | No       | 278.36        | 1:21:13       | 299,998              | [Link](https://huggingface.co/kuds/rl-lunar-lander-sac)            |
| DQN        | Yes      | 155.64        | 1:59:15       | 999,999              | [Link](https://huggingface.co/kuds/rl-lunar-lander-dqn)            |

## Training Notes
- Set `ent_coef` for PPO as it encourages exploration of other actions. Stable Baselines3 defaults the value to 0.0. [More Information](https://www.youtube.com/watch?v=1ppslywmIPs)
- Do not set your `eval_freq` too low, as it can sometimes cause instability during learning due to being interrupted by evaluation. (e.g. >=10,000)
- Stable Baselines3's DQN parameters `exploration_initial_eps` and `exploration_final_eps` help determine how exploratory your model is at the beginning and end of training.

## Finding Theta Blog Posts
- [Solving Gymnasium's Lunar Lander with Deep Q Learning (DQN)](https://www.findingtheta.com/blog/solving-gymnasiums-lunar-lander-with-deep-q-learning-dqn)
- [Comparing how PPO, SAC, and DQN Perform on Gymnasium's Lunar Lander](https://www.findingtheta.com/blog/comparing-how-ppo-sac-and-dqn-perform-on-gymnasiums-lunar-lander)
