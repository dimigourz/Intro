# Burgers 1D — controlled ablations

[Open the ablation launcher notebook](Burgers_ablation_driver.ipynb)

The Colab launcher contains three experiment suites: `core`, `ordering`, and `sensitivity`. It sets a 400-epoch, three-seed protocol (1234, 2026, 2027) with 400 training trajectories. The sensitivity sweep covers local radii 1/3/5, Fourier modes 8/16/32, and window lengths 1/5/10. Notebook outputs document completed runs.

**Missing dependency:** The notebook calls `/content/burgers1d_reviewer_ablations_colab.py` after uploading it interactively via `files.upload()`. That companion Python program was **not among the four uploaded notebooks**, so this folder alone is insufficient to rerun the ablation tests. The notebook is archived as supplied, and is not described as self-contained.

Local-radius and Fourier-mode sweeps change parameter counts; changing window length also changes the number of training windows. These sweeps are not parameter-matched.
