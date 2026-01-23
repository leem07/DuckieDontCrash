---
layout: default
title: Proposal
---
## Summary of the Project
Duckietown is a simulation driven program that navigates a duckiebot through a world, whether physical or purely virtual. Our goal is to train our duckiebot using various RL algorithms in order to determine the best results based on the given task. Our duckiebot will be given the simulated world with these variables and be expected to not veer off course or crash into obstacles/walls.

## Project goals
Minimum goal: we want to use the base level of lane following to get the duckiebot around a track without going off course while not doing extraneous things by timing it. (is that possible duckiebot racetrack using diff algorithms to judge how well they do against each other for eval? but that might be computationally crazy and also not feasible with baselvl duckietown lol?)

Realistic goal: After accomplishing basic lane following, we want to upgrade our duckiebot to allow the navigation through randomly generated mazes with obstacles to avoid. (q learning?)

Moonshot: Improving our model enough to go from simulation to real.

## AI/ML algorithms
We will evaluate how different models do in training the duckiebot against each other with an anticipation of Proximal Policy Approximation due to stability issues that may come with other algorithms, with an additional focus in Q-Learning for maze navigation/obstacle avoidance.

## Evaluation Plan
The experiments we are looking to run in order to evaluate the ability of our duckiebot is to judge how fast or how well the duckiebot will be against obstacles in the track, while also not veering from its designated path. Our metrics will be (maybe a timer?)
metrics
what baselines/naive approaches ?
how much our approach could improve from baseline

qualitative analysis through debugging/toy cases/basic sims
how results are visualized to see if it works (i guess just analyzing the simulation)
qualitatiave properties of a good result

## AI Tool Usage
No AI tools have been used so far.
