# DNN Assignment 2

A deep learning assignment focused on sequence modeling, recurrent architectures, and transformer-based text generation. This repository contains the implementation, experimental setup, and generated artifacts for two problems completed as part of the coursework.

## Project Overview

This assignment explores:
- Problem 1: Time-series / sequence classification using a recurrent neural network setup on the UCI HAR dataset
- Problem 2: Autoregressive language modeling using a transformer-based model trained on Tiny Shakespeare
- Ablation and comparison studies across model variants, seeds, and training configurations

The configuration used in this project is based on the assignment specification and the provided student variant information:
- Problem 1 hidden size: h = 32
- Problem 2 model size: d = 64, 4 attention heads, d_ff = 256
- Seeds used: 11, 23, 42
- Problem 1 ablation variant: gradient clipping enabled (clip norm = 1.0 vs no clipping)
- Base architecture: vanilla RNN with T = 200
- Problem 2 ablations: single seed (11)

## Repository Structure

```text
.
├── README.md
├── requirements.txt
├── report.pdf
├── problem1/
│   ├── problem1.ipynb
│   └── figures/
├── problem2/
│   ├── problem2.ipynb
│   ├── generated_samples.txt
│   └── figures/
└── results.csv
```

## Prerequisites

- Python 3.10 or newer
- pip package manager
- CUDA-capable GPU recommended; Google Colab T4 is suitable for running the notebooks efficiently

## Environment Setup

Create a virtual environment and install dependencies:

```bash
python -m venv .venv
source .venv/bin/activate   # On Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

The project dependencies are listed in `requirements.txt` and include:
- PyTorch
- NumPy
- pandas
- scikit-learn
- matplotlib
- reportlab

## How to Run

### 1) Problem 1
Open and run `problem1/problem1.ipynb` in Jupyter or VS Code Notebook mode.

Execution notes:
- The notebook downloads the UCI HAR dataset automatically if it is not already present.
- Results are appended to `results.csv`.
- Generated plots are saved in `problem1/figures/`.

### 2) Problem 2
Open and run `problem2/problem2.ipynb` after completing Problem 1 for comparison rows.

Execution notes:
- The notebook downloads Tiny Shakespeare automatically if needed.
- Generated samples are written to `problem2/generated_samples.txt`.
- Visual outputs are saved in `problem2/figures/`.

## Expected Output

The project produces:
- quantitative experiment results in `results.csv`
- generated text samples in `problem2/generated_samples.txt`
- training/validation figures in both `problem1/figures/` and `problem2/figures/`
- report summary in `report.pdf`

## Runtime Estimate

On a T4 GPU, the end-to-end workflow is expected to take approximately 26 minutes.

## Notes

- This project is intended for coursework and academic experimentation.
- If the runtime environment differs from the recommended setup, results may vary slightly.
- The notebooks are designed to be run in sequence, with Problem 1 executed before the comparison workflow in Problem 2.

## License

This project is provided for educational purposes as part of the DNN assignment and is not intended for commercial distribution unless explicitly authorized by the course or institution.

