# Mini-project 01: a basic DQN across environments

**Status:** Goals defined; theory, implementation, and experiments are planned.

## Project goal

Implement a simple Deep Q-Network (DQN) and see how well this basic approach performs on LunarLander and a few additional discrete-action environments. Establish an understandable, reproducible baseline before introducing algorithmic improvements.

Follow the general approach of my reinforcement learning homework: explain the theory, implement the method, run experiments, and connect the results to what I have learned.

This is the first of two preparatory mini-projects leading to the [main Rainbow reproduction](../large_projects/rainbow/). The [second mini-project](../miniProject_02_dqn_variants/) will introduce algorithm variants and replay-buffer comparisons.

## 1. Theory: what is DQN?

- [ ] Explain Q-learning, function approximation, the learning objective, and the DQN update.
- [ ] Explain the online Q-network, target network, uniform experience replay, and epsilon-greedy exploration.
- [ ] Describe the assumptions and limitations of the baseline.
- [ ] Connect the explanation to the implementation with equations and pseudocode.

## 2. Environment selection

- [ ] Include discrete-action LunarLander.
- [ ] Choose a few additional discrete-action environments; CartPole, Acrobot, and MountainCar are candidates.
- [ ] Record exact environment identifiers, library versions, observations, actions, rewards, and episode boundaries.
- [ ] Define task-specific evaluation metrics and success criteria before the main runs.

The additional environments and their versions are still to be chosen.

## 3. Implementation goals

- [ ] Implement a basic DQN agent with one-step targets, a standard Q-network, uniform replay, and epsilon-greedy exploration.
- [ ] Add configurable environment selection, hyperparameters, and random seeds.
- [ ] Share training, evaluation, and logging code across environments.
- [ ] Handle episode termination and time-limit truncation explicitly in target construction.
- [ ] Document dependencies and exact commands to reproduce runs and figures.

The algorithm variants and PER experiments belong to Mini-project 02.

## 4. Experiments and results

- [ ] Train and evaluate the baseline on every selected environment.
- [ ] Run multiple seeds and report variability, within a documented compute budget.
- [ ] Plot training performance and separate evaluation returns against environment steps.
- [ ] Report final evaluation performance, sample efficiency, training stability, and runtime.
- [ ] Document per-environment budgets and hyperparameter choices; distinguish fixed settings from any tuning.
- [ ] Include failed runs and environments where the basic approach struggles.

Report results per environment, with a summary table using task-specific metrics. Any cross-environment aggregate will need a defined normalization.

## 5. Conclusions and handoff

- [ ] Explain where basic DQN works well and where it struggles under the tested settings.
- [ ] Relate observed behavior to exploration, bootstrapping, function approximation, and replay.
- [ ] Identify limitations and hypotheses to carry into the variants project.
- [ ] Save a reproducible baseline configuration and results for later comparisons.

## Deliverables and remaining decisions

Deliver a theory explanation, implementation, experiment instructions, result tables and figures, and personal conclusions. Select the final environment set, dependencies, budgets, seed count, and evaluation schedule before implementation and main experiments. Align the detailed write-up with my homework when those materials are available.

No implementations or experimental results have been added yet.
