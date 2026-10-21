# Burgers 1D — competitive baselines

[Open the comparison notebook](Burgers_FFNO_UNetAR_CNOdirect.ipynb)

A self-contained Colab implementation for **F-FNO**, an autoregressive **U-Net**, and a **direct CNO** predictor. It includes experiment configuration, dataset loading, evaluation routines, model definitions and saved notebook outputs.

These baselines use an **initial-state-only** protocol, not the H10 (ten-known-state) protocol used in folders 01 and 02. Comparisons across those protocols must explicitly account for the different observations available to each model.

Update the Google Drive data/output paths before running. Dataset and checkpoints are not included.
