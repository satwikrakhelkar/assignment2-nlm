# Assignment 2 – Neural Language Model Training (PyTorch)

## Author
Satwik Rakhelkar  
Assignment for IIIT Hyderabad Internship

## Overview
This assignment explores how neural language models learn to predict text sequences. The goal is to implement a character-level LSTM model from scratch using PyTorch and analyze how model capacity and training duration affect learning behavior.

## Dataset
The dataset used is *Pride and Prejudice* by Jane Austen. Character-level tokenization is applied, and all preprocessing is done manually using Python and PyTorch tools.

## Model Architecture
- Embedding layer to represent characters
- LSTM layer for sequence modeling
- Linear layer for output logits
- Trained using CrossEntropyLoss and Adam optimizer

## Experiment Setup

Three configurations were tested to demonstrate underfitting, overfitting, and best-fit behavior:

| Scenario   | Embedding Dim | Hidden Dim | Epochs | Perplexity | Notes                        |
|------------|---------------|------------|--------|------------|------------------------------|
| Underfit   | 32            | 64         | 5      | 3.56       | Model too small to learn     |
| Overfit    | 256           | 512        | 30     | 1.05       | Memorized small dataset      |
| Best Fit   | 128           | 256        | 15     | 3.35       | Balanced generalization      |

Each experiment includes a loss plot and final perplexity score.

## How to Run
1. Open `Assignment2.ipynb` in Google Colab.
2. Upload `Pride_and_Prejudice-Jane_Austen.txt` to the Colab workspace.
3. Run all cells in order.
4. Loss plots and perplexity values will be printed for each experiment.

## Files Included
- `Assignment2.ipynb`: Full training and evaluation notebook
- `report.pdf`: Summary of setup, results, and observations
- `loss_plot_underfit.png`: Underfit loss curve
- `loss_plot_overfit.png`: Overfit loss curve
- `loss_plot_bestfit.png`: Best fit loss curve
- `README.md`: This file

## Notes
- All code is implemented from scratch using PyTorch.
- No pre-trained models or external libraries were used.
- Random seeds are fixed for reproducibility.
