# AWFNO-H10-K5 — Burgers 1D

[Open the Colab notebook](AWFNO_H10_K5_Burgers.ipynb)

Ten exact initial snapshots, five-step prediction windows, width 32, four layers, sixteen Fourier modes, local radius 3. Evaluated at 25, 50, 100, 200, 400, and 800 training trajectories. The saved notebook includes training and test outputs, training/inference time, and results export paths.

**Reported test error:** mean absolute physical L2 (full forecast and final snapshot), not relative L2. Results are a sample-size sweep and should not be represented as a multi-seed confidence interval.

The HDF5 dataset and checkpoint files are external to this repository. Update `CONFIG["DATA_PATH"]` and `CONFIG["OUTPUT_ROOT"]` before running.
