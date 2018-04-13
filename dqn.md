# DQN for DaVinci robot

## Reward
The reward function depends on the distance from the robot arm gripper to the target object. The goal is to minimize this distance and a higher reward is given for shorter the distances.

The distance is calculated from images taken from a camera placed (above / to the side) the PSM. The unit is in pixels and is calculated using openCV.

## Discounting
The RL algorithm will optimize for total discounted rewards. In other words, we will choose some number γ (gamma) where 0 < γ < 1, and at each step in the future, we optimize for r0 + γ r1 + γ² r2 + γ³ r3… (where r0 is the immediate reward, r1 the reward one step from now etc.).

Discount rate (gamma) of 0.99 is used for the project.

## Q Learning

Policies are the output of any RL algorithm. Policies simply indicate what action to take for any given state (a set of rules)

### Q Function Q(s, a)
Q(s, a) = r + γ maxₐ’(Q(s’, a’))

An optimal Q function gives the optimal policy
π(s) = argmaxₐ(Q(s,a))   // policy at state s

Q funct provides an estimate of how much discounted reward the agent can obtain by following its policy from any given state

## Goal
The goal is to estimate the Q(s,a) function. 

Estimating any function can be done using DNN,so the Q(s,a) is estimated using DNN




## references:
[1] https://becominghuman.ai/lets-build-an-atari-ai-part-0-intro-to-rl-9b2c5336e0ec

[2] https://becominghuman.ai/lets-build-an-atari-ai-part-1-dqn-df57e8ff3b26
