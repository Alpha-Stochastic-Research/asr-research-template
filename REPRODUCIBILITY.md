# Reproducibility Guide

## Objective

This document explains how to reproduce the project environment, analyses, tests, and results.

## System Requirements

Document the required environment:

* Operating system:
* Python version:
* Required system packages:
* Hardware requirements:
* Estimated memory usage:
* Estimated execution time:

## Environment Setup

Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate
```

On Windows:

```powershell
python -m venv .venv
.venv\Scripts\activate
```

Install the project and development dependencies:

```bash
python -m pip install --upgrade pip
pip install -e ".[dev]"
```

## Data Preparation

Document:

1. Where the required data can be obtained.
2. Which version or retrieval date was used.
3. Where the data should be stored locally.
4. Which preprocessing scripts must be executed.
5. Which data cannot be redistributed.

Example:

```bash
python scripts/prepare_data.py
```

Do not commit confidential, restricted, or licensed data without redistribution rights.

## Configuration

Document all required configuration values.

Use `.env.example` for variable names, but never commit real credentials.

Example:

```bash
cp .env.example .env
```

## Randomness

All stochastic procedures must use explicit random seeds.

Document:

* Python random seed
* NumPy random seed
* Machine learning framework seed
* Simulation seed
* Sampling seed

Example:

```python
SEED = 42
```

A seed improves reproducibility but does not always guarantee identical results across operating systems, hardware, or library versions.

## Running the Analysis

Provide the exact commands required to reproduce the main analysis.

Example:

```bash
python scripts/run_analysis.py
```

For a complete pipeline:

```bash
python scripts/prepare_data.py
python scripts/run_analysis.py
python scripts/generate_results.py
```

## Running Tests

Run the test suite:

```bash
pytest
```

Run the code-quality checks:

```bash
ruff check .
```

All required checks should pass before results are published.

## Expected Outputs

Document the expected output files.

| Output         | Location           | Description                      |
| -------------- | ------------------ | -------------------------------- |
| Processed data | `data/processed/`  | Generated analysis dataset       |
| Figures        | `results/figures/` | Publication-ready figures        |
| Tables         | `results/tables/`  | Statistical or numerical results |
| Logs           | `results/logs/`    | Execution and validation logs    |
| Report         | `reports/`         | Research report or paper         |

Generated outputs should not be committed when they are large, confidential, or reproducible from source files.

## Result Validation

For each important result, document:

* Expected value or range
* Accepted numerical tolerance
* Reference benchmark
* Validation method
* Known platform-dependent differences

## Software Versions

Record the exact dependency versions used for published results.

Example:

```bash
python --version
pip freeze > requirements-lock.txt
```

The lock file should be updated when a result is formally released.

## Reproduction Checklist

* [ ] The required Python version is documented.
* [ ] Installation commands are documented.
* [ ] Data sources and retrieval dates are documented.
* [ ] Data-preparation commands are documented.
* [ ] Random seeds are fixed and documented.
* [ ] Analysis commands are documented.
* [ ] Tests pass.
* [ ] Code-quality checks pass.
* [ ] Expected outputs are documented.
* [ ] Dependency versions are recorded.
* [ ] Known limitations are documented.
* [ ] The reproduction process has been reviewed by `release-admins`.

## Known Limitations

Document anything that may prevent exact reproduction, including:

* Unavailable proprietary data
* External APIs
* Changing online datasets
* Hardware differences
* Floating-point differences
* Non-deterministic algorithms
* Software-version differences
* Long execution times
