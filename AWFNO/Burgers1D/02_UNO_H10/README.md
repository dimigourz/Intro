# U-NO-H10 — Burgers 1D

[Open the Colab notebook](UNO1D_H10_Burgers.ipynb)

A one-dimensional adaptation of the U-NO spectral encoder-decoder, conditioned on ten exact initial states and applied recursively one step at a time. The saved notebook reports the 25–800 training-trajectory sweep, absolute physical L2 test errors, inference and training times, and results exports.

**Scope:** This notebook adapts an official *temporal-conditioning protocol*; it is **not an officially published U-NO implementation or an official published U-NO benchmark for 1D Burgers**. Do not describe these results as such.

The model has 2,830,001 trainable tensor elements. Training and forecasting configurations should be compared explicitly against AWFNO rather than assumed identical. The dataset and checkpoints are external to this repository.
