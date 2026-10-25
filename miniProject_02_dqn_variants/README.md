# Mini-project 02: DQN variants and replay buffers on LunarLander

**Status:** Goals defined; theory, implementation, and experiments are planned.

## Project goal

Follow the general approach of my reinforcement learning homework: first explain the theory, then implement the methods, run experiments on a shared environment, and use the results to draw conclusions and connect back to the theory.

Build on the baseline from [Mini-project 01](../miniProject_01_dqn/) to study DQN, Double DQN (DDQN), and Dueling DQN on a discrete-action LunarLander environment. A second set of experiments will examine how a standard uniform replay buffer compares with prioritized experience replay (PER).

This is the second preparatory mini-project for the [main Rainbow reproduction](../large_projects/rainbow/). Reuse the baseline and experiment conventions from Mini-project 01, documenting any changes needed for this comparison.

## 1. Theory: what is DQN?

- [ ] Explain the connection between Q-learning and DQN, including the learning objective and update rule.
- [ ] Explain the roles of the Q-network, target network, experience replay, and exploration.
- [ ] Describe Double DQN and the change it makes to the DQN target.
- [ ] Describe Dueling DQN and its value and advantage streams.
- [ ] Explain the distinction between Double DQN and Dueling DQN.
- [ ] Explain uniform replay and PER, including sampling priorities, importance-sampling weights, and priority updates.
- [ ] State the hypotheses to test for the algorithm and buffer comparisons.

## 2. Environment: LunarLander

- [ ] Select a discrete-action LunarLander environment and record its exact identifier and library version.
- [ ] Document observations, actions, rewards, and episode termination or truncation.
- [ ] Define the evaluation protocol and a task success criterion before running the comparisons.
- [ ] Record the environment settings so every method is tested on the same task.

## 3. Implementation goals

- [ ] Reuse and verify the baseline DQN agent from Mini-project 01.
- [ ] Implement Double DQN (DDQN).
- [ ] Implement Dueling DQN, using the baseline DQN target for the initial comparison so the architecture change can be studied separately.
- [ ] Implement a standard replay buffer with uniform sampling.
- [ ] Implement a PER buffer.
- [ ] Share environment handling, logging, and evaluation across methods where practical.
- [ ] Make algorithm choice, buffer choice, hyperparameters, and random seed configurable.

## 4. Experiments

### Experiment A: compare algorithms

Train and evaluate DQN, Double DQN, and Dueling DQN with the standard uniform replay buffer. Compare learning behavior and performance under a documented training and evaluation protocol.

### Experiment B: compare replay buffers

Run each algorithm with uniform replay and with PER. Compare the two buffers within each algorithm to examine the effect of prioritization.

| Algorithm | Standard uniform buffer | PER buffer |
| --- | --- | --- |
| DQN | Planned | Planned |
| Double DQN (DDQN) | Planned | Planned |
| Dueling DQN | Planned | Planned |

- [ ] Run all six configurations using multiple random seeds, as resources allow.
- [ ] Keep environment settings and evaluation conditions consistent.
- [ ] Document training and tuning budgets, including any differences between methods.
- [ ] Record hyperparameters, seeds, dependency versions, and commands needed to reproduce each run.

## 5. Results to collect

- [ ] Training learning curves and separate evaluation returns versus environment steps.
- [ ] Average evaluation performance and variability across seeds.
- [ ] Sample efficiency, including steps to the chosen performance threshold when reached.
- [ ] Training stability and failed or unsuccessful runs.
- [ ] Training time and replay-buffer overhead, using a consistent timing method.
- [ ] Summary tables and plots comparing algorithms and replay buffers.

## 6. Conclusions and connections

- [ ] Explain how the observed behavior relates to the theory and initial hypotheses.
- [ ] Discuss the tradeoffs between DQN, Double DQN, and Dueling DQN on this task.
- [ ] Discuss whether PER improves each method under the tested conditions and what additional cost it introduces.
- [ ] Connect the findings to course concepts such as bootstrapping, off-policy learning, exploration, and sampling bias.
- [ ] Identify limitations and useful follow-up experiments.

## Decisions to make before implementation

Choose the exact environment version, dependencies, network sizes, hyperparameters, seed count, training budget, and evaluation schedule. Align the detailed write-up and experiment format with my homework when those materials are available.

No implementations or experimental results have been added yet.
