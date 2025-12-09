# LLM Fine-Tuning Observability

This repository provides a scaffold for building and monitoring large language model fine-tuning workflows. It separates configuration, data artifacts, model checkpoints, logs, notebooks, automation scripts, and Python source code so you can manage experiments at scale.

## Layout

- `configs/` — YAML configuration files for training, evaluation, classifier quality thresholds, and dashboards.
- `data/` — Raw datasets, processed features, and fixed evaluation samples.
- `logs/` — Run-time metrics, generated samples, and classifier logs.
- `models/` — Base model snapshots plus fine-tuned checkpoints organized per experiment.
- `notebooks/` — Exploratory and debugging notebooks for interactive analysis.
- `scripts/` — Command-line entry points for training, evaluation, dashboards, and regression checks.
- `src/llm_observability/` — Python package implementing configuration helpers, data loaders, training loops, evaluation utilities, quality assessment, monitoring dashboards, and shared helpers.

## Getting Started

1. Install dependencies listed in `requirements.txt` (or configure `pyproject.toml` if using Poetry/pip-tools).
2. Update the YAML files in `configs/` to reflect dataset locations, hyperparameters, and logging destinations.
3. Use the scripts in `scripts/` to launch training, evaluation, or dashboard services.
4. Inspect outputs under `logs/` and `models/` to monitor progress and iterate on improvements.
