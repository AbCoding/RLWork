# Reinforcement Learning Portfolio

My attempt to recreate the algorithms I am learning in my Reinforcement Learning class and apply them across a range of problems. This repository connects implementations with the theory behind them, experimental results, and reflections on what I learned.

The portfolio is organized into focused mini-projects and larger projects that compare multiple algorithms on the same task. Each project should explain the problem, how the algorithm works, what happened in experiments, and how the findings relate to other concepts in reinforcement learning.

## Project index

### Mini-projects

| Project | Problem / environment | Algorithms | Status |
| --- | --- | --- | --- |
| [miniProject_X](miniProject_X/) | To be chosen | To be chosen | Reusable template |

### Large projects

| Project | Shared task / environment | Algorithms compared | Status |
| --- | --- | --- | --- |
| [Project template](large_projects/project_template/) | To be chosen | To be chosen | Reusable template |

These entries are starting templates. Implementations and experimental results will be added as the portfolio develops.

## Repository structure

```text
RLWork/
├── README.md                          # Portfolio overview and project index
├── miniProject_X/                     # Template for a focused mini-project
│   ├── README.md                      # Problem, goals, setup, and run instructions
│   ├── algorithms/README.md           # Algorithm descriptions and theory
│   ├── src/README.md                  # Implementation location
│   ├── results/README.md              # Experimental setup, figures, and findings
│   └── conclusions.md                 # Lessons and connections to other concepts
└── large_projects/
    ├── README.md                      # Overview of larger comparative projects
    └── project_template/
        ├── README.md                  # Shared task and comparison questions
        ├── algorithms/README.md       # Theory and differences between methods
        ├── src/README.md              # Shared environment and algorithm implementations
        ├── results/README.md          # Comparative experiments and analysis
        └── conclusions.md             # Tradeoffs, limitations, and connections
```

## Starting a project

For a mini-project, copy `miniProject_X` to a numbered, descriptive folder such as `miniProject_01_bandits`. For a larger project, copy `large_projects/project_template` to a folder such as `large_projects/cartpole_comparison`.

Then:

1. Define the problem, learning objective, and environment in the project README.
2. Explain the algorithms and underlying theory in `algorithms/README.md`.
3. Add the implementation under `src/`, documenting dependencies and exact commands in the project README.
4. Record the experiment settings, seeds, measurements, and plots under `results/`.
5. Write conclusions and connect the findings to other course concepts.
6. Add the project to the index above and keep its status current.

Each project manages its own dependencies and run instructions. There is no repository-wide installation step yet.

## Experiment conventions

- Record environment and library versions, hyperparameters, random seeds, and training budgets.
- Separate training performance from evaluation performance, and describe the evaluation policy.
- When feasible, run multiple seeds and report variability alongside average performance.
- For comparisons, use a shared evaluation protocol and explain differences in tuning or compute budgets.
- Commit small result tables and figures; keep large checkpoints, datasets, and raw logs outside Git.
- Cite course material, papers, and external implementations used in each project, making clear which parts I implemented myself.

## Possible directions

These are ideas for future projects, not completed work or a fixed syllabus:

- Multi-armed bandits and exploration strategies.
- Dynamic programming on small Markov decision processes.
- Monte Carlo and temporal-difference learning.
- SARSA and Q-learning on a shared control problem.
- Function approximation, deep Q-learning, and policy-gradient methods.

The goal is to build a portfolio that demonstrates both working implementations and an understanding of when and why different approaches behave differently.
