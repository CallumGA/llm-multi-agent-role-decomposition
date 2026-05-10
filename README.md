# Deterministic Multi-Agent Role Decomposition for Clinical Classification

This repository contains code and artifacts for a controlled study of how internal multi-agent role structure and information routing change classification behavior in LLM-based clinical decision support tasks. It compares a Generic Deliberative (GD) architecture and a Feature-Specialist (FS) architecture under identical model weights, decoding settings, computation budget, and adjudication logic. Results are provided for two tabular benchmarks: UCI Cleveland Heart Disease and Pima Indians Diabetes.

## Repository Structure

- `data/`
  - `processed_cleveland.csv` – preprocessed Cleveland Heart Disease dataset
  - `processed_diabetes.csv` – preprocessed Pima Indians Diabetes dataset
  - `heart-disease.names` – dataset documentation for Cleveland features/encodings
- `results/`
  - `heart_disease/` – per-protocol prediction outputs for Cleveland
    - `single-base-predictions.csv`
    - `generic-predictions.csv`
    - `specialist-predictions.csv`
  - `diabetes/` – per-protocol prediction outputs for Pima
    - `single-base-predictions.csv`
    - `generic-predictions.csv`
    - `specialist-predictions.csv`
- `experiment.ipynb` – end-to-end notebook to run inference and compute metrics

## Requirements

- Python 3.13+
- Ollama installed and running locally
- Model pulled in Ollama (default used in the paper: `llama3.1:8b`)

### Install Ollama and pull the model

Install Ollama for your OS, then run:

```bash
ollama pull llama3.1:8b