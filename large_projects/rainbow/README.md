# Rainbow: reproduction and follow-up investigations

**Status:** Goals defined; implementation and experiments are planned.

## Project goal

Reimplement the main ideas of [Rainbow: Combining Improvements in Deep Reinforcement Learning](https://arxiv.org/abs/1710.02298) (Hessel et al.; first posted in 2017, published in 2018). Follow the paper's structure with my own theory explanations, implementations, experimental recreations, and conclusions.

This is Part 2 of the initial research theme. Part 1 consists of [Mini-project 01: basic DQN](../../miniProject_01_dqn/) and [Mini-project 02: variants and replay buffers](../../miniProject_02_dqn_variants/). Their code, configurations, and findings will provide the starting point for this project.

## 1. Introduction and research questions

- [ ] Explain why combining improvements is worth studying.
- [ ] Define the questions each experiment will answer and state hypotheses before the main runs.
- [ ] Ask which components help alone, which help within the combined agent, and how the answers depend on the environment and training budget.

## 2. Background: implement all six improvements

For each component below, write an explanation, equations, pseudocode, implementation notes, and limitations. Cite the original component paper as well as Rainbow.

| Component | Implementation goal | Starting point |
| --- | --- | --- |
| Double Q-learning | Double DQN target | Mini-project 02 |
| Prioritized experience replay | Prioritized sampling and importance-sampling correction | Mini-project 02 |
| Dueling networks | Value and advantage streams | Mini-project 02 |
| Multi-step learning | Configurable n-step returns | New component |
| Distributional reinforcement learning | Categorical C51 return distribution and projection | New component |
| Noisy networks | Factorized noisy layers for exploration | New component |

These six components follow the [Rainbow paper](https://arxiv.org/pdf/1710.02298).

## 3. The combined Rainbow agent

- [ ] Integrate all six components into one agent.
- [ ] Explain the interactions between components and verify that disabling them produces the intended baselines.
- [ ] Check integration details against the paper, including distributional dueling outputs and distributional-loss replay priorities.
- [ ] Document how exploration changes when noisy layers are enabled or disabled.
- [ ] Keep the original Rainbow configuration identifiable when later extensions are added.

## 4. Experimental methods

- [ ] Select a shared benchmark suite and compute budget before the main comparison.
- [ ] Start with environments informed by the mini-projects; decide whether to include MinAtar or an Atari subset as a later benchmark stage.
- [ ] Document every departure from the original task suite, architecture, preprocessing, hyperparameters, and training/evaluation protocol.
- [ ] Define training budgets, tuning budgets, seed count, evaluation episodes, and checkpoint selection rules.
- [ ] Record environment steps, gradient updates, and wall-clock time separately; define frame counts when applicable.
- [ ] Report per-environment results and uncertainty across runs. Define any normalization before aggregating across tasks.

Rainbow was evaluated on 57 Atari games. Our benchmark selection remains open; conclusions from smaller or different tasks will be scoped to those settings. [Source](https://arxiv.org/pdf/1710.02298).

## 5. Results and ablation studies

The paper removes one component at a time from the combined agent. Recreate that design, alongside additional baseline comparisons. [Source](https://arxiv.org/pdf/1710.02298).

| Experiment group | Planned comparison | Purpose |
| --- | --- | --- |
| Baseline | Basic DQN on the selected suite | Establish a reference |
| Individual additions | DQN + each improvement separately | Study each change from the baseline |
| Combined agent | Full Rainbow versus DQN | Test the combined approach |
| Ablations | Full Rainbow minus each of its six components | Study each component in the combination |
| Follow-up investigations | Rainbow versus selected later modifications | Test a specific later claim |

- [ ] Produce learning curves, evaluation tables, and comparisons of sample efficiency, final performance, stability, and compute cost.
- [ ] Explain what each experiment can establish; distinguish an isolated addition from removing that component from a combination.
- [ ] Report unsuccessful runs and inconclusive comparisons.

## 6. Related work and follow-up investigations

- [ ] Review later work for improvements, limitations, or challenges to Rainbow's conclusions.
- [ ] Maintain [literature notes](literature.md) with the specific claim, evidence, reproduction requirements, and status for each candidate.
- [ ] Select feasible claims to test after the core reproduction, including findings that might qualify or disagree with expectations.
- [ ] Compare each selected modification against a matched baseline and account for changes in training, tuning, or compute.

The initial reading list includes *Revisiting Rainbow* (2021) and *Beyond the Rainbow* (2024; revised 2025). These are research leads; specific reproduction experiments remain to be selected.

## 7. Personal conclusions and discussion

- [ ] For each investigated claim, connect the source's argument to my experiment, observation, interpretation, and limitations.
- [ ] Explain where my results agree, disagree, or remain inconclusive.
- [ ] Discuss how conclusions change across environments and budgets.
- [ ] Connect the findings to the mini-projects and relevant class concepts.
- [ ] Identify useful follow-up experiments based on the evidence.

## Deliverables

Produce a write-up organized like the paper, component and combined-agent implementations, reproducible configurations and commands, result tables and figures, and personal conclusions. Include a comparison with selected later work when feasible.

No implementations or experimental results have been added yet.
