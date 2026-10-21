# Alternating Windowed Fourier Neural Operators — 1D Burgers experiments

Archive of the **four Google Colab notebooks** supplied for the numerical experiments accompanying the AWFNO manuscript revision. Source code and saved notebook outputs are retained. This folder documents results rather than claiming an independently verified reproduction.

## Experiments

| Folder | Experiment |
| --- | --- |
| [01_AWFNO_H10_K5](01_AWFNO_H10_K5/) | AWFNO using 10 known states and 5-step prediction windows; sample-size sweep. |
| [02_UNO_H10](02_UNO_H10/) | 1D U-NO adaptation using 10 known states and one-step recursive prediction; sample-size sweep. |
| [03_Architecture_Ablations](03_Architecture_Ablations/) | Controlled core, ordering, and sensitivity experiment launcher. |
| [04_Competitive_Baselines](04_Competitive_Baselines/) | F-FNO, autoregressive U-Net, and direct CNO baseline notebook. |

## H10 comparison — 1D viscous Burgers

The following are **mean absolute physical L2 errors**, not relative L2. Each row is one reported sample-size run, not an average over three training seeds.

| Training trajectories | AWFNO-H10-K5 full | U-NO-H10 full | AWFNO final | U-NO final |
| ---: | ---: | ---: | ---: | ---: |
| 25 | 1.682620 | 1.370799 | 0.140898 | 0.095506 |
| 50 | 0.873756 | 0.849425 | 0.054573 | 0.052009 |
| 100 | 0.589395 | 0.632981 | 0.035648 | 0.036892 |
| 200 | 0.324680 | 0.403800 | 0.020628 | 0.024316 |
| 400 | 0.170492 | 0.205577 | 0.010623 | 0.014145 |
| 800 | 0.115609 | 0.155182 | 0.006596 | 0.009959 |

AWFNO-H10-K5 reports 128,453 trainable tensor elements; U-NO-H10 reports 2,830,001. AWFNO predicts five states per application, whereas the U-NO adaptation predicts one state at a time. **This is neither a parameter-matched nor a strictly compute-matched comparison.** Recorded runtime differences are also hardware- and implementation-dependent; the notebook reports are not a calibrated speed benchmark.

The initial-state-only architectures in folder 04 use a different information protocol and should not be compared directly against H10 results without documenting that distinction.

## Reproducibility scope

- All notebooks were authored for **Google Colab**, with HDF5 input and checkpoints/results stored on Google Drive. Set the `DATA_PATH` and `OUTPUT_ROOT` variables to your own locations.
- The Burgers HDF5 dataset, trained checkpoints, and complete raw CSV/JSON output directories are **not** part of this archive.
- **The ablation notebook is a launcher, not a standalone implementation:** it invokes `/content/burgers1d_reviewer_ablations_colab.py`. That companion script was not included in the supplied four notebooks.
- The scripts and outputs have not been rerun or externally validated as part of this upload. Check the metric definitions, temporal protocol, split indices, training budget and random seeds before citing cross-notebook comparisons.

Last archived: 21 October 2026.
