# DSL Final Project 2026

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

DSL Final Project 2026 - UT Austin


## Install environment and check if it is up to date

### 1. Create and activate the Conda environment

```bash
conda create -n dsl_final_proj python=3.12
conda activate dsl_final_proj
```

### 2. Install requirements

From the project root directory, run:

```bash
python -m pip install -r requirements.txt
```

### 3. Check dependencies

Check for dependency conflicts:

```bash
python -m pip check
```

Check if any requirements need installing or updating (without making changes):

```bash
python -m pip install -r requirements.txt --dry-run
```

### 4. Update if needed

```bash
python -m pip install -r requirements.txt
```


## Project Structure

This project explores reinforcement learning (RL) in a simulated car-driving environment. The repository is organized around the main stages of the RL workflow: environment setup, agent development, training, and evaluation.

### Directory Overview

```text
dsl_final_project_2026/
│
├── data/
│   ├── raw/                  # Original data and recorded episodes
│   ├── interim/              # Intermediate processed data
│   └── processed/            # Cleaned data ready for analysis
│
├── dsl_final_project_2026/   # Main Python package
│   ├── environments/         # Driving environment and reward functions
│   ├── agents/               # RL agents and policies
│   ├── training/             # Agent training scripts
│   ├── evaluation/           # Evaluation of trained agents
│   └── utils/                # Reusable helper functions
│
├── models/
│   └── checkpoints/          # Saved model weights and checkpoints
│
├── notebooks/                # Exploratory analysis and experiments
│
├── reports/
│   └── figures/              # Figures used in reports and presentations
│
├── configs/                  # Experiment configurations and hyperparameters
│
├── tests/                    # Tests for environment and reward functions
│
├── requirements.txt          # Python dependencies
├── pyproject.toml            # Project configuration
├── Makefile                  # Project automation commands
└── README.md                 # Project overview and instructions
```

### Folder Descriptions

| Directory | Purpose | Examples |
|---|---|---|
| `data/` | Stores datasets and files generated or used by the project. | Recorded driving episodes, trajectories, processed observations. |
| `environments/` | Defines or wraps the driving simulator and its interaction with the agent. | Track setup, observations, action spaces, episode termination. |
| `agents/` | Contains the agent's decision-making logic and policies. | PPO, DQN, or other RL algorithms. |
| `training/` | Contains scripts for training agents through interaction with the environment. | Training loops, episode tracking, checkpoint saving. |
| `evaluation/` | Tests trained agents and measures their performance. | Lap times, completion rates, crashes, average reward. |
| `utils/` | Contains reusable helper functions. | Plotting, logging, data-processing utilities. |
| `models/` | Stores trained models and checkpoints. | Saved policy weights and model snapshots. |
| `notebooks/` | Supports exploration, experimentation, and analysis. | Environment exploration, reward experiments, training analysis. |
| `configs/` | Stores experiment settings separately from the code. | Learning rate, algorithm choice, training steps. |
| `tests/` | Contains automated tests to check that important components work correctly. | Environment reset tests, reward-function tests. |
| `reports/` | Stores final outputs for reports and presentations. | Learning curves, lap-time comparisons, performance plots. |
| `docs/` | Contains additional project documentation. | Simulator instructions, design decisions, setup notes. |


