# Rainbow literature and candidate investigations

**Status:** Initial reading list, reviewed on October 25, 2026. This is a starting point for further research; no follow-up reproduction has been selected or run.

## Core paper

[Hessel et al., *Rainbow: Combining Improvements in Deep Reinforcement Learning*](https://arxiv.org/abs/1710.02298) (2017 preprint; 2018 publication).

Use this paper to define the component implementations, combined agent, and main ablation design. For each claim chosen for reproduction, record its exact section or figure and the conditions under which it was reported before running our experiment.

## Follow-up 1: Revisiting Rainbow

[Obando-Ceron and Castro, *Revisiting Rainbow: Promoting more insightful and inclusive deep reinforcement learning research*](https://proceedings.mlr.press/v139/ceron21a.html) (ICML 2021; [paper](https://proceedings.mlr.press/v139/ceron21a/ceron21a.pdf)).

The authors revisit Rainbow on smaller tasks and investigate component interactions. Section 5.4 examines Huber versus MSE loss and their interaction with Adam and RMSProp. Their findings qualify simple claims that one loss is always preferable.

Candidate experiments for this portfolio:

- Revisit component contributions on the environments used in our mini-projects.
- Compare DQN with Huber/MSE crossed with Adam/RMSProp, controlling the tuning budget and reporting all four combinations.
- Check whether any observed ranking changes across environments and seeds.

This is an older, directly relevant follow-up that can guide experiments at the scale of this portfolio. Treat its findings as conditional empirical results rather than universal rules.

## Follow-up 2: Beyond the Rainbow

[Clark et al., *Beyond The Rainbow: High Performance Deep Reinforcement Learning on a Desktop PC*](https://arxiv.org/abs/2411.03820) (2024 preprint; revised May 2025; [version 2 text](https://arxiv.org/html/2411.03820v2)).

This work extends Rainbow with changes including implicit quantile networks (IQN), Munchausen RL, spectral normalization, architectural changes, and vectorized environments. Table 1 identifies retained and replaced components; it is an extension rather than a direct rebuttal of Rainbow.

Candidate experiments for this portfolio:

- Select a feasible modification, such as replacing C51 with IQN, and write down a precise hypothesis and matched baseline.
- Recheck the paper's ablations and dependencies before assuming a change can be studied in isolation.
- Separate sample-efficiency comparisons from wall-clock gains due to parallel environment collection.
- For claims involving visual architectures, choose a suitable observation-based task and account for model size and compute.

Reproducing the full Beyond the Rainbow agent is a possible later extension; the current core goal remains the original Rainbow reproduction.

## Selecting and evaluating a claim

Before promoting a reading-list entry to a planned experiment, record:

1. **Source:** paper version, section, figure/table, and any author code used as a reference.
2. **Claim:** the specific reported improvement, limitation, or disagreement to investigate.
3. **Conditions:** task, observations, baseline, preprocessing, hyperparameters, and training/tuning budget.
4. **Our experiment:** what will match the source, what will differ, and why the comparison is useful.
5. **Evidence required:** metrics, seeds, uncertainty, and criteria for supported, unsupported, or inconclusive results.
6. **Outcome:** our measurements, interpretation, limitations, and links to reproducible artifacts.

Continue the literature search when designing the follow-up experiments. Check later versions and relevant newer papers, and record the search date and selection rationale. An improvement under different conditions alone does not establish a rebuttal of the original paper.
